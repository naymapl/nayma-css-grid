![Nayma Logo](https://nayma.pl/img/logo-naymapl-color-web.svg)

# Simple, light and responsive CSS framework from Nayma.pl

Nayma CSS Grid is a simple, lightweight (* 3kb gzip *), responsive CSS framework/boilerplate that will create a simple 12 columns layout grid (flexbox support), headlines, lists, forms, tables, buttons and much more. Also you will get the ability to add a top navigation bar with a mobile slider side menu in pure CSS.

#### DEMO on CodePen.io: https://codepen.io/Naymapl/pen/rwpXEg
#### DEMO on CodePen.io Polska Wersja: https://codepen.io/Naymapl/pen/oeEmqM

#### Polska Dokumentacja: https://github.com/naymaeu/nayma-css-grid/blob/master/Readme-PL.md

#### GitHub: https://github.com/naymaeu/nayma-css-grid
#### GitLab: https://gitlab.com/naymapl/nayma-css-grid

# Why Nayma CSS grid ?

Nayma CSS Grid has all the necessary elements such as grid columns, headers, buttons, forms, tables, menus and more. It only takes (3kb gzip). It is fully responsive and has a special mobile menu in pure CSS. It is based on the newest units such as `REM`,` VH` or `VW`.

# Installation

You can download the zip package from this repository or use the NPM installation option to install and download the package.

***NPM***
```
npm install nayma-css-grid
```

Then, in the `head` section of the page, attach the` nayma-css-grid.min.css` file.

```html
    <link rel="stylesheet" href="nayma-css-grid.min.css">
```

# Grid columns and examples

We create a grid of columns based on rows. Same columns are based on flexbox so they fill a row automatically. For example, the code that inserts one column with the `column` class in the `row` div, so that it is stretched to 100% of the row:

```html
<div class="row">
   <div class="column">Auto</div>
</div>
```

By using the `column` class, we add columns that use flexbox. However you can add assign a specific column width from 1 to 12. We use very simple to learn syntax for column layout. Here are all the classes we can use to create a grid of columns:

* column
* column is-1
* column is-2
* column is-3
* column is-4
* column is-5
* column is-6
* column is-7
* column is-8
* column is-9
* column is-10
* column is-11
* column is-12
* column is-one-third
* column is-two-third
* column is-half

For example, the layout of columns 1/3 and 2/3 will look like this:

```html
<div class="row">
   <div class="column is-one-third">One Third</div>
   <div class="column is-two-third">Two Third</div>
</div>
```

We can also combine columns based on the flexbox with those that have a fixed width:

```html
<div class="row">
   <div class="column is-one-third">One Third</div>
   <div class="column">Auto</div>
   <div class="column">Auto</div>
   <div class="column">Auto</div>
</div>
```

We hope everything is simple and understandable for everyone.

# Sections

You can use the `<section>` which has a white background or `<section class ="lightgrey">` with a light gray background. All section have 100% width.

Sample section code:

```html
<section>
    <div class="container">
        <div class="row">
            <div class="one-third column">One Third</div>
            <div class="two-third column">Two Third</div>
        </div>
    </div>
</section>
```
From version 0.5.0 there is also a `hero` section with a blue gradient background. Of course you can edit color in the css file.
Sample html code for the `hero` section:

```html
<section class="hero">
    <div class="container">
        <div class="row">
            <div class="column">
                <div class="title">Nayma CSS Grid</div>
                <div class="subtitle">Simple, light and responsive CSS framework from Nayma.pl</div>
                <a class="button is-inverted" href="#">Download</a>
            </div>
        </div>
    </div>
</section>
```

# Headers

All headings from `<h1>` to `<h6>` have been clipped and no additional action is required.

# Lists

Nayma CSS Grid uses two standard types `ul` and` ol`. These items have been stowed and no additional action is required

Sample lists:

```html
<ol>
    <li>Basic styles for numbered lists</li>
    <li>
        You can use nested lists
        <ul>
            <li>The first non-numbered item</li>
            <li>Second non-numbered item</li>
        </ul>
    </li>
    <li>Last numbered list item</li>
</ol>
```
# Buttons

In the Nayma CSS grid we can use four different types of buttons. These are regular `<a>` with assigned `.button`, `<button>` and `<input>` elements. All these elements can be a button without filling and filling background.

Example of buttons without fill:

```html
<a class="button" href="#">Anchor button</a>
<button>Button element</button>
<input type="submit" value="submit input">
<input type="button" value="button input">
```
Example of filled buttons. Just use the `.button-primary` class:

```html
<a class="button button-primary" href="#">Anchor button</a>
<button class="button-primary">Button element</button>
<input class="button-primary" type="submit" value="submit input">
<input class="button-primary" type="button" value="button input">
```
n addition, we have the `.is-inverted` class for buttons that we put on a dark background. For the buttons that we want to place in the navigation bar, we use the `.is-button-nav` class.

# Forms

Each form `<form>` has been stapled and we can use elements like:

* label
* input
* select
* textarea
* checkbox

Example form:

```html
<form>
    <div class="row">
        <div class="six columns no-padding">
            <label for="exampleEmailInput">Twój email</label>
            <input class="u-full-width" type="email" placeholder="test@nayma.pl" id="exampleEmailInput">
        </div>
        <div class="six columns no-padding">
            <label for="selectList">Wybierz temat kontaktu</label>
            <span class="select">
                <select class="u-full-width" id="selectList">
                    <option value="Option 1">Wycena projektu</option>
                    <option value="Option 2">Potrzebny dodatkowy kontakt</option>
                    <option value="Option 3">Mam inne pytania</option>
                </select>
            </span>
        </div>
    </div>
    <label for="exampleMessage">Wiadomość</label>
    <textarea class="u-full-width" placeholder="Wpisz swoją wiadomość..." id="exampleMessage"></textarea>
    <label class="example-send-yourself-copy">
        <input type="checkbox">
        <span class="label-body">Wyślij kopię do mnie</span>
    </label>
    <input class="button-primary" type="submit" value="Wyślij">
</form>
```

# Main Navigation

Nayma CSS Grid allows us to add a `<header>` section to the navigation page. Navigation can be added using the `<nav>` tags. We can further divide our top beam into 2 columns with the `<nav class="left-nav">` and `<nav class="right-nav">`. Sample logo menu on the left and simple menu on the right:

```html
<!-- Main navigation section  -->
    <header>
        <div class="container">
            <div class="row">
                <!-- Left nav with logo  -->
                <nav class="left-nav">
                    <div class="logo">
                        <a href="">nayma-css-grid</a>
                    </div>
                </nav>
                <!-- Right nav with menu  -->
                <nav class="right-nav">
                    <a class="nav-link" href="">Start</a>
                    <a class="nav-link" href="" target="_blank">Doc</a>
                    <a class="nav-link" href="" target="_blank">GitHub</a>
                    <a class="button button-primary is-button-nav" href="">Download</a>
                </nav>
            </div>
        </div>
    </header>
    <!-- Move page 4.4rem down -->
    <div class="nav-fix"></div>
<!-- End Main navigation section  -->
```

# Mobile Navigation

Mobile navigation in pure CSS is added at the very top of our page just after the end of the `</ head>` section. Let's remember that you have to edit your menu both in the main navigation section and also in sidebar. This, however, allows you to use other links andelements in the mobile version and other in main nav menu. Sample code for mobile navigation:

```html
<!-- Mobile navigation section -->
    <input type="checkbox" id="hamburger">
    <label class="menuicon" for="hamburger"><span></span></label>
    <div class="menu">
        <ul>
            <li><a href="index.html">Start</a></li>
            <li><a href="https://gitlab.com/naymapl/nayma-css-grid" target="_blank">Doc</a></li>
            <li><a href="https://github.com/naymaeu/nayma-css-grid" target="_blank">GitHub</a></li>
            <a class="button is-inverted" href="https://github.com/naymaeu/nayma-css-grid/archive/master.zip">Download</a>
        </ul>
    </div>
<!-- End mobile navigation section -->
```

# Footer

To create a footer we use the `<footer>` tag inside you will places the paragraph with the text of our footer. Example code below:

```html
<!-- Footer Section -->
    <footer class="footer">
        <div class="container">
            <div class="row">
                <div class="column">
                    <p>
                        <strong>Nayma CSS Grid</strong> by <a href="https://nayma.pl" target="_blank">Nayma.pl</a>. The source code is licensed
                        <a href="http://opensource.org/licenses/mit-license.php" target="_blank">MIT</a>.
                    </p>
                </div>
            </div>
        </div>
    </footer>
<!-- End Footer Section -->
```

# Horizontal line

Horizontal lines `<hr>` can be used without any additional classes.

# Tables

By adding simple tables to our site we can use tags like `table`, `tr` and `td`. They all have basic styling.

Sample simple HTML table code:

```html
<table>
    <tr>
        <th>1 column</th>
        <th>2 column</th>
        <th>3 column</th>
        <th>4 column</th>
    </tr>
    <tr>
        <td>Frog</td>
        <td>Blizzard</td>
        <td>Cat</td>
        <td>Cameleon</td>
    </tr>
    <tr>
        <td>Salmon</td>
        <td>Sea Bass</td>
        <td>Hearing</td>
        <td>Magic carp</td>
    </tr>
</table>
```

# Additional classes

Additional classes that allow you to add padding or margins from the top and bottom, and a class that erases all margins and padding:

* .padding-top-20
* .padding-top-30
* .padding-top-50
* .padding-top-80
* .padding-top-100
* .padding-bottom-20
* .padding-bottom-30
* .padding-bottom-50
* .padding-bottom-80
* .padding-bottom-100
* .margin-top-20
* .margin-top-30
* .margin-top-50
* .margin-top-80
* .margin-top-100
* .margin-bottom-20
* .margin-bottom-30
* .margin-bottom-50
* .margin-bottom-80
* .margin-bottom-100
* .no-padding
* .is-text-centered
* .is-fullwidth
* .is-pull-right
* .is-pull-left
* .is-hidden-mobile

# Thanks

We hope that this simple documentation will allow you to understand how to use all the elements as well as the grid of columns. We hope that using this simple framework/boilerplate will be easy, fun and useful when building simple pages. If you have any questions, please feel free to contact us.

See also our site: [Nayma.pl](https://nayma.pl)
See our blog: [Blog Nayma.pl](https://blog.nayma.pl)