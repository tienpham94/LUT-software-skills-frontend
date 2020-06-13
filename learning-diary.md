# Tien Pham #0596083

### LEARNING DIARY - MODULE

### 13.6.2020

####  Intro & Sass Workflow Setup
I chose to use VSCode since I have a lot of experience using it in real work life. For me, it is easy to use and definitely the best editor out there for web application development. It is very popular in the web dev community, completely open source.
I have node.js installed, need to install node-sass for sass development.
I also have git installed, and I use MacOS.
First we need to `mkdir modern_portfolio`
After that `cd modern_portfolio`
Then `code .` to open the folder

`live-server` is a great extension to open website in the browser
`prettier` is also very handy to format code
To use `prettier` and to format on save we enable it in the settings
`emmet` can make quick html, very handy
To create an html page with emmet just type `!` and click Tab, there will be a template ready to use 

```
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="ie=edge">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```

To install node-sass
1. `yarn init`
2. `yarn add node-sass`
3. Add `node_modules` to `.gitignore`

To use node-sass
1. Add script: `"sass": "node-sass -w scss -o dist/css/ --recursive"`
2. Run `yarn sass`
3. It's gonna compile your sass to dist/css folder
4. Add it to index.html `<link rel="stylesheet" href="css/main.css">` and it will use the compiled styles