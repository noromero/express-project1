Instructions on how to start an Express service/app

\\ Run: installs express --save tag updates package.json
npm install express --save


\\ Create: Create an index.js file that initializes the server and its pages
const express = require('express');
const app = new express();
const port = 8080;
app.get("/", (req,res) => {
    return res.send("Hello World!");
});
let server = app.listen(port, () => {
    console.log("listening at http://localhost:"+ port)
})


\\ Update package.json to include nodemon start script
"scripts": {
    "start" : "nodemon index.js",
    "test": "echo \"Error: no test specified\" && exit 1"
  },


\\ Run: start the server and it updates auto whenever file is changed
npm start


\\ Open Browser: To access server and pages
http://localhost/:PATH
