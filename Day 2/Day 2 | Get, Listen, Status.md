**_Web Request_**<br>
**GET**&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;     -> _**Requesting Information**_<br>
**POST**&nbsp;&nbsp;&nbsp;    -> _**Add to Database**_<br>
**PUT**&nbsp;&nbsp;&nbsp; &nbsp;   -> _**Edit to Database**_<br>
**DELETE** -> _**Delete to Database**_<br>

## _Express_

<b>
  
```javascript
const express = require("express");
const app = express();
const PORT = 3000;

app.get("/", (req, res) => {
  res.status(200).send("<h1>Hello, HC Sir!</h1>");
});

app.get("/features", (req, res) => {
  res.send("A test runner built for humans");
});

// For Instagram
app.get("/insta", (req, res) => {
  const insta = {
    userName: "hiteshchoudharyofficial",
    followers: 70,
    follow: 200,
  };
  res.status(200).json({ insta });
});

// For Twitter
app.get("/twitter", (req, res) => {
  const twitter = {
    userName: "ChowdharyHitesh",
    following: 0,
    followers: 900,
  };
  res.status(200).json({ twitter });
});

// For LinkedIn
app.get("/linkedin", (req, res) => {
  const linkedin = {
    userName: "ChowdharyHitesh",
    connections: 5000000,
  };
  res.status(200).json({ linkedin });
});

app.get("/api/v1/:token", (req, res) => {
  console.log(req.params.token);
  res.status(200).json({ param: req.params.token });
});

// bad practise of writing 500 if everything is correct
// always write the req before the response
app.listen(PORT, () => {
  console.log(`Example app listening on port ${PORT}`);
});

// Assignment
// make atleast 2-3 express apps to practise
```
