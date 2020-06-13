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
I learned that to create an html page with emmet just type `!` and click Tab, there will be a template ready to use 

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

In this section I learned how to install node-sass
1. `yarn init`
2. `yarn add node-sass`
3. Add `node_modules` to `.gitignore`

To use node-sass
1. Add script: `"sass": "node-sass -w scss -o dist/css/ --recursive"`
2. Run `yarn sass`
3. It's gonna compile your sass to dist/css folder
4. Add it to index.html `<link rel="stylesheet" href="css/main.css">` and it will use the compiled styles

####  Homepage and Core Sass/CSS
An interesting thing that I learned was to add a div with `menu-btn` class just type `.menu-btn` and click Tab, emmet will generate that for you
To add 3 divs with `btn-line` class type `.btn-line*3` and click Tab

Also, I discovered how to have anchor tag that points to a different file: 
```
<li class="nav-item">
   <a href="/work.html" class="nav-link">
      Home
    </a>
</li>
```

I learned how to use font-awesome icons: 
1. Add this to `head` `<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.2.0/css/all.css" integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
    crossorigin="anonymous">`
2. Use icons:
```
<div class="icons">
  <a href="#!">
    <i class="fab fa-twitter fa-2x"></i>
  </a>
  <a href="#!">
    <i class="fab fa-facebook fa-2x"></i>
  </a>
  <a href="#!">
    <i class="fab fa-linkedin fa-2x"></i>
  </a>
  <a href="#!">
    <i class="fab fa-github fa-2x"></i>
  </a>
</div>
```

I learn how to use nested sass, do `&.lg-heading` inside style block
```
h1,
h2,
h3 {
  margin:0;
  font-weight: 400;

  &.lg-heading {
    font-size: 6rem;
  }
}
```

I learned how to ake away link underline: `text-decoration: none;`

Then I learned how to use mixin in sass: 
```
@mixin easeOut {
  transition: all 0.5s ease-out;
}

&:hover {
  color: $secondary-color;
  @include easeOut();
}
```

I learned that `vh` stands for `viewport height`, 100vh will be 100 viewport height

Also, I learned how to use url in sass `$home-image: url(../img/background.jpg);`

Also, I learned how to use conditional in mixin: 
```
@if $show-home-image {
  if true then run this
}
```

Also, I leanred how to use `rgba` in `sass`
```
background: rgba($primary-color, $background-opacity);
```

I learned that we better to use a pseudo element instead of `<div class="overlay">` for overlay
```
&:after {
  content: '';
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  z-index: -1;
  background: rgba($primary-color, $background-opacity);
}
```

I learned that to use partial in `sass` name the file with starting `_` `(_config.scss)`

####  Rotating Menu Button

I learned more about using partial in `sass`, as in the previous section we use the same file with starting `_` `(menu.scss)`
And then we will need to include the partial file in the main sass file `@import 'menu';`
Building a hamburger menu button is very interesting, I will learn about CSS transition in this section.
I learned that if I have any issue with node-sass, partial issue for example, I will need to run sass again `yarn sass`

I discovered that if we want to select an element in the DOM, we can use `document.querySelector()`
If we want to select element with class `menu-btn`, we can use the querySelector as described above:
```
const menuBtn = document.querySelector('.menu-btn');
```

If we want to select all elements that has a specific class we will need to use `document.querySelectorAll()`, that will put elements into something called nodeList which is similar to an array
```
const navItems = document.querySelectorAll('.nav-item');
```

I learned that if we want to reassign a variable, we better use `let` instead of `const`

I discovered that to add a class to an element using Javascript we can use `.classList.add(class)`
```
menuBtn.classList.add('close');
```

Responsive hamburger menu button transform into a close icon is super interesting!

I learned that to rotate something 180 degree we can use 
```
transform: rotate(180deg);
```

I also know now that to rotate a hamburger menu into an X we can do like this: 
```
&:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}

// Line 2 - Hide
&:nth-child(2) {
  opacity: 0;
}

// Line 3 - Rotate
&:nth-child(3) {
  transform: rotate(-45deg) translate(7px, -6px);
}
```

I learned that CSS transition is really realy powerful.

####  Menu Overlay & Responsiveness

####  Page With CSS Grid


####  Work and Contact Pages

####  Website Deployment



