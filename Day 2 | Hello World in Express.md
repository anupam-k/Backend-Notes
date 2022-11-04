## _App.js_
<b>
  
```javascript
const express = require("express");
// importing the express

const app = express();
// lot of functionality is being
// transffered in my app variale

const port = 3000;
// variable named port which holds a number 3000

app.get("/", (req, res) => {
  // path=> "/", callback => req, res
  res.send("Hello JS!");
  // response.send(message)
});

app.listen(port, () => {
  console.log(`Example app listening on port ${port}`);
});
```
</b>
