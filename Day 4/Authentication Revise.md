# _Notes_
![note-dark-1](https://user-images.githubusercontent.com/91872149/200155350-fd68d841-38a5-450f-8988-f83650eaac0e.png)

## _Steps_

1. npm init
2. make app.js
3. npm i express
4. npm i mongoose jsonwebtoken bcryptjs



# _Start with databse.js(config)_

<b>
  
```javascript
const mongoose = require("mongoose");

const MONGODB_URL = "somestring";

exports.connect = () => {
  mongoose
    .connect(MONGODB_URL, {
      useNewUrlParse: true,
      useUnifiedTopology: true,
    })
    .then(console, log("DB CONNECTED with a success"))
    .catch((error) => {
      console.log("DB connection failed");
      console.log(error);
      process.exit(1);
    });
};
```
  
</b>

# _2nd Step is with user.js(model)_

<b>

```javascript
const mongoose = require("mongoose");

const userSchema = new mongoose.Schema({
  firstname: {
    type: String,
    default: null,
  },
  lastname: {
    type: String,
    default: null,
  },
  email: {
    type: String,
    unique: true,
  },
  password: {
    type: String,
  },
  token: {
    type: String,
  },
});

module.exports = mongoose.model("user", userSchema);
// user will always be stored in small case and it will always be prularized

```
</b>

# _3rd Step: App.js (controller)_

<b>
  
 ```javascript
 require("./config/database").connect();
const express = require("express");
const jwt = require("jsonwebtoken");
const bcrypt = require("bcrypt");

// import model - User
const User = require("./model/user");

const app = express();
app.use(express.json()); // discuss this later
app.use(express.urlencoded({ extended: true }));

app.get("/", (req, res) => {
  res.send("Hello Auth System");
});

app.post("/register", async (req, res) => {
  try {
    // collect all information
    const { firstname, lastname, email, password } = req.body;

    // validate if data exists, if exists
    if (!(email && password && lastname && firstname)) {
      res.status(402).send("All fields are required!");
    }

    // check if email is in correct format or not

    // check if user exits or not
    const existingUser = await User.findOne({ email });

    if (existingUser) {
      res.status(401).send("User already found in Database!");
    }

    // encrypt the password
    const myEncyPassword = await bcrypt.hash(password, 10);

    // create a new entry in the database
    const user = await User.create({
      firstname,
      lastname,
      email,
      password: myEncyPassword,
    });

    // create a token and send it to user
    const token = jwt.sign(
      {
        id: user._id,
        email,
      },
      "shhhh",
      { expiresIn: "2h" }
    );

    user.token = token;
    // don't want to send the password
    user.password = undefined;

    res.status(201).json(user);
  } catch (error) {
    console.log(error);
    console.log("Error is response route");
  }
});

app.post("/login", async (req, res) => {
  try {
    // colleted information from frontend
    const { email, password } = req.body;
    // validate
    if (!(email && password)) {
      res.status(401).send("Email and password are required!!");
    }
    // check user in database
    const user = await User.findOne({ email });
    // if user does not exits - assignment
    // match the password
    if (user && (await bcrypt.compare(password, user.password))) {
      const token = jwt.sign({ id: user._id, email }, "shhhh", {
        expiresIn: "2h",
      });

      user.password = undefined;
      user.token = token;

      const options = {
        expires: new Date(Date.now() + 3 * 24 * 60 * 60 * 1000),
        httpOnly: true,
      };
      res.status(200).cookie("token", token, options).json({
        success: true,
        token,
        user,
      });
    }

    // create token and send
    res.sendStatus(400).send("email or password is incorrect");
  } catch (error) {
    console.log(error);
  }
});

```
</b>


# _HW_
- make this project up and running
- add listening port
- check with Postman
