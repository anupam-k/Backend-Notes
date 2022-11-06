# _Notes_
![note-dark-1](https://user-images.githubusercontent.com/91872149/200155350-fd68d841-38a5-450f-8988-f83650eaac0e.png)

## _Steps_

1. npm init
2. make app.js
3. npm i express
4. npm i mongoose jsonwebtoken bcryptjs



# _Start with databse.js_

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
