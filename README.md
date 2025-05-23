# HTML-CSS-JS

- Timeline:
  - 1993: HTML
  - 1994: PHP
  - 1995: JavaScript
  - 1996: CSS
  - 1998: XML
- "Client languages" (browser language)
  - HTML
  - CSS
  - JavaScript
- JavaScript makes a page "animated"
- PHP is a "Server language" (works on the web server, browsers never know)
- Illustration:
  - HTML is a manikin
  - CSS is the clothing
  - JavaScript "animates", so the manikin moves like a robot and changes clothes
- XML borrows HTML framework, using it to organize information the way HTML organizes a webpage
  - XML can be displayed like a webpage or used silently for software to access information data
  - XML is a transparent (visible, non-secure) alternative to SQL
  - XML is used in news feeds, RSS, blog feed, podcasts, and settings files

## HTML

### HTML uses `<tags>`
- Each has an open `<tag>` and close `</tag>`
- Some tags are self-closing
  - HTML: `<self-closing-tag>`
  - XML: `<self-closing-tag />`
- ***HTML tags are called "elements", not "tags"!***

### First line:
- The first line of an HTML file is:
```html
<!DOCTYPE html>
```

### Comments
```html
<!-- I am a comment -->

<!--
- Comments may span multiple lines

Just like this

-->
```

### DOM (Document Object Model)
- The basic "floor plan" of an HTML file is called the DOM
- Basic HTML DOM:
```html
<!DOCTYPE html>
<html>

  <head>
  </head>

  <body>
  </body>

</html>
```
- Page content is in `<body>`

- `<head>` example:
```html
<head>
  <title>Browser Title</title>
  <meta charset="utf-8">
  <meta name="robots" content="noindex">
  <meta name="description" content="Describe website in search results">
  <meta http-equiv="content-type" content="text/html; charset=utf-8">
  <link href="https://verb.ink/" rel="canonical">
  <link rel="shortcut icon" type="image/png" href="favicon.png">
  <link href="css/styles.css" rel="stylesheet" type="text/css">
</head>
```

- `<body>` example:
```html

<body>
  <!-- Very top of page -->
  <header>

    <nav>
      <ul class="menu">
        <li><a href="index.html">Home</a></li>
        <li><a href="about.html">About</a></li>
      </ul>
    </nav>

  </header>
  <!-- Main content -->
  <div id="main">

    <section>
      <p>We like inking! <a href="http://verb.ink">Learn more</a></p>
    </section>

    <article>
      <h1>Post Title</h1>
      <p>I am a long blog post.</p>
      <p>I am another paragraph in the long blog post.</p>
    </article>

    <aside>
      <p>Another great article to distract you! <a href="otherarticle.html">Read more...</a></p>
    </aside>

  </div>
  <!-- Very bottom of page -->
  <footer>

    <nav>
      <ul class="menu">
        <li><a href="terms.html">Terms & Privacy</a></li>
      </ul>
    </nav>

  </footer>

</body>
```

### Attributes & Values
- Example:
  - Element: `p`
  - Attribute: `style=`
  - Value: `"color:red;"`

```html
<p style="color:red;">

</p>
```

#### All elements can have attributes `id` and `class`
- These are used by
- CSS
- JavaScript
- Example:
  - Element: `p`
  - ID attribute: `id="top"` (must be unique or page will break!)
  - Class attribute: `class="big"` (can be used many times)

  ```html
  <p id="top" class="big" style="color:red;">

  </p>
  ```
#### Important attributes
- `src=`: source
  - This sources an external file
  - Examples:
```html
    <script src="scripts.js"></script> <!-- JavaScript file -->
    <img src="image.gif"> <!-- GIF image -->
```
- `href=`: hypertext reference (a location on the web)
- `rel=`: relation (what it is used for)
  - Examples:
```html
<link href="https://verb.ink/" rel="canonical"> <!-- this web address -->
<link href="favicon.png" rel="shortcut icon" type="image/png"> <!-- favicon in browser -->
<link href="css/styles.css" rel="stylesheet" type="text/css"> <!-- CSS file -->
<a href="page.html"></a> <!-- relative web address -->
<a href="https://verb.ink/page.html"></a> <!-- full web address -->
```

### Common Elements
- Metadata & Scripts:
  - `<title>` (title in the web browser top bar or tab)
  - `<meta>` (extra information in the page)
  - `<link>` (files referred to in the page)
  - `<style>` (contains CSS)
  - `<script>` (contains JavaScript)
- Organizing:
  - `<div>` (other, only this in HTML4)
  - `<header>` usually was: `<body><div class="header">`
  - `<footer>` usually was: `<body><div class="footer">`
  - `<nav>` (navigation menu)
  - `<section>` (large area)
  - `<article>` (one item)
  - `<aside>` (widget/ad area)
  - In HTML4, these were only `<div>`
- Headers: `<h1>`, `<h2>`, ... `<h6>`
- Paragraphs:
  - `<p>` (normal paragraph)
  - `<blockquote>` (block quote)
  - `<pre>` (monospace paragraph)
- Style:
  - `<i>` italics
  - `<b>` bold
  - `<em>` emphasis ('important' italics)
  - `<strong>` strong ('important' bold)
  - Special style span:
    - `<span>` (to set special style)
    - `<code>` (monospace span)
    - `<q>` (quote)
    - `<cite>` (source citation)
  - Change color/font example: (CSS goes inside `style=""`)
    - `<span style="color:red; font-weight:bold; font-size: 10pt">`
- Lists:
  - `<ol>` / `<ul>` ordered / unordered
    - `<li>` list item
- Breaks:
  - `<br>` line break
  - `<hr>` horizontal rule
- Link: `<a>`
- Webforms: `<form>`
  - `<textarea>`
  - `<select>`
    - `<option>`
  - `<input>` `type=`:
    - `"text"`
    - `"password"`
    - `"email"`
    - `"url"`
    - `"radio"`
    - `"color"`
    - `"submit"`
- Media: (self-closing)
  - Image: `<img>`
  - Audio: `<audio>` (HTML5)
  - Video: `<video>` (HTML5)


### HTML entities
*Most special characters need an HTML code called an "HTML entity"*

Here are some:
```html
   &#160;   &nbsp;  ('non-breaking space'; white space is ignored, this won't be ignored)
"  &#34;    &quot;
'  &#39;    &apos;
&  &#38;    &amp;
<  &#60;    &lt;
>  &#62;    &gt;
°  &#176;   &deg;
¶  &#182;   &para;
–  &#8211;  &ndash;
—  &#8212;  &mdash;
‾  &#8254;  &oline;
‘  &#8216;  &lsquo;
’  &#8217;  &rsquo;
“  &#8220;  &ldquo;
”  &#8221;  &rdquo;
™  &#8482;  &trade;
©  &#169;   &copy;
®  &#174;   &reg;
¢  &#162;   &cent;
£  &#163;   &pound;
€  &#8364;  &euro;
¥  &#165;   &yen;
¤  &#164;   &curren;
¦  &#166;   &brvbar;
§  &#167;   &sect;
←  &#8592;  &larr;
↑  &#8593;  &uarr;
→  &#8594;  &rarr;
↓  &#8595;  &darr;
♠  &#9824;  &spades;
♣  &#9827;  &clubs;
♥  &#9829;  &hearts;
♦  &#9830;  &diams;
```

## CSS
*Style the text of an HTML document*

**Cascading Style Sheet**

- Font
- Size
- Color
- Location
- Bold/italics/etc
- Border
- Margin
- Padding
- Space before/after

***It helps to understand fonts:***
- Awesome, fast video - [Karen Kavett DIY: An Intro to Typography](https://www.youtube.com/watch?v=tWFWJGA7qrc)
- Short overview - [PinkWrite: Intro to 5 fonts](https://drive.google.com/open?id=0BwTdjnieHEEndkR3OFZjdVJ0QWM)
- Short overview - [PinkWrite: Intro to Roman fonts](https://drive.google.com/open?id=0BwTdjnieHEEnNjF3RktZbmhiaTg)
- In-depth - [fonts.com: Type Classifications](https://www.fonts.com/content/learning/fontology/level-1/type-anatomy/type-classifications)

***It helps to understand Color Theory and RGB:***
- Understand HTML color codes - [RGB](https://www.youtube.com/watch?v=HX46ILgwTNk)
- Color Theory - [Beginning Graphic Design: Color](https://www.youtube.com/watch?v=_2LLXnUdUIc)
- Examples mixing colors - [RGB & CMYK](https://github.com/inkVerb/pictypes/blob/master/rgb-cmyk.md)
- Different image types - [JPEG, PNG & GIF](https://github.com/inkVerb/pictypes/blob/master/jpg-png-gif.md)

### Comments

| **CSS** :
```css
/* I am a comment */

/*
* Comments may span multiple lines

Just like this

*/
```

### Format

- **Sizes** can be:
  - `px`  pixels (default)
  - `em`  relative to font-size of the element
  - `cm` 	centimeters (relative to pixels and inches)
  - `mm` 	millimeters (relative to pixels and inches)
  - `in` 	inches (1in = 96px = 2.54cm)
  - `pt` 	points (1pt = 1/72 of 1in)
  - `pc` 	picas (1pc = 12 pt)
  - Newer browers:
    - `vw` 	viewport width: relative to 1% of the width of the browser
    - `vh` 	viewport height: relative to 1% of the height of the browser

- **Colors** can be:
  - Hexcode - eg: `#aaff33;`
  - RGB - eg: `rgb(170,255,51);`
  - Name - eg: `red;`
  - Others, but we mainly use hexcode

- Styling:

| **CSS** :
```css
/* Element */
p {
  color: #222;
}

/* ID */
#top {
  color: #222;
}

/* Class */
.big {
  color: #222;
}

/* Element only with ID */
p#top {
  color: #222;
}

/* Element only with Class */
p.big {
  color: #222;
}

/* Many Elements */
p, div, a {
  color: #222;
}

/* Many Elements only with ID */
p#top, p#bottom, div#info, a#home {
  color: #222;
}

/* Many Elements only with Class */
p.big, p.small, div.big, a.big {
  color: #222;
}

```

- **Element `<p>`:** color, background, font, size

| **CSS** :
```css
p {
  color: #222;
  background: #fff;
  font-family:Helvetica, "Open Sans", sans-serif;
  font-size: 0.8em;
}
```

- **Style by:** element, class, or id

| **HTML** :
```html
<p id="top" class="big">

</p>

<p id="bottom" class="big">

</p>

<div id="note" class="big">

</div>
```

| **CSS** :
```css
.top {
  color: #222;
  background: #fff;
  font-family:Helvetica, "Open Sans", sans-serif;
  font-size: 0.8em;
}
```

*This can all be on one line, but this is the style of most CSS stylesheets*

### Style HTML with CSS

- Embed CSS in the `<head>` between `<style>` tags

| **HTML** :
```html
<style>
  p { color: #222; font-size: 0.8em; }
</style>
```

- `<link>` CSS in the `<head>`

| **HTML** :
```html
<link href="css/styles.css" rel="stylesheet" type="text/css">
```

## JavaScript

This crash course illustrates JavaScript

- Changing HTML
- Interacting with the browser

### Comments

| **JavaScript** :
```js
// I am a comment

/*
# Comments may span multiple lines

Just like this

*/
```

### Use JavaScript with HTML

1. The **affected** HTML element has an ID JavaScript "method" will recognize

- This is based on ID, but there are many JavaScript "methods"
  - `getElementById("some_id")`
  - `getElementsByClassName("some_class")`
  - `getElementsByName("some_name")`

| **file.html** : *(Note `id="showMe"`)*

```html
<div id="showMe" style="display:none;">
```

2. The **activating** HTML element has an `onclick=` attribute with the JavaScript function as the `"value()"`

- `onclick=` is called a JavaScript "event"
- Other "events" can include:
  - `onload=`
  - `onmouseover=`
  - `onmouseout=`
  - `onkeydown=`
  - `onchange=`


| **file.html** : *(Note `onclick="jsFunction()"`)*
```html
<code onclick="jsFunction()">Click me and I will do something</code>
```

3. The JavaScript must be included in the `<script>` tag
- Sometimes it must be in the `<head>`
- Sometimes it must be in the `<body>` **after** the HTML it interacts with
- JavaScript can be embedded:

| **HTML** :
```html
<script>
  function jsFunction() {
    // JS function code here
  }
</script>
```

- JavaScript can be included in an external file:

| **HTML** :
```html
<script src="scripts.js"></script>
```

Our specific Javascript in this example changes the `display:` style between `block` (show) and `none` (hide)

### Full example:

- Tip: Search for
  - `jsFunction`
  - `showMe`

| **file.html** :
```html
<code onclick="jsFunction()">Click me and I will do something</code>

<!-- Keep divs from acting strangely, sometimes you need a div inside another div! -->
<!-- style= can be inline (like this) or in the CSS -->
<div style="display: inline-block; width: 100%; float: right;">
  <!-- MUST be inside this tag, in CSS won't work! : style="display:none;" -->
  <div id="showMe" style="display:none;">
    <p>
      I am hiding and showing when you click "click me"
    </p>
  </div>
</div>

<script>
  function jsFunction() {
    var x = document.getElementById("showMe");
    if (x.style.display === "none") {
      x.style.display = "block";
    } else {
        x.style.display = "none";
    }
  }
</script>
```

### JavaScript Interaction

Here are other examples of JavaScript interacting with the browser or changing HTML

1. Change *Ctrl + S* to activate button with `id="send_form"`

| **JavaScript** :
```js
document.addEventListener("keydown", function(cs) {
  if ( (window.navigator.platform.match("Mac") ? cs.metaKey : cs.ctrlKey) && (cs.keyCode == 83) ) {
    cs.preventDefault(); // Stop it from doing what it normally does
    document.getElementById('send_form').click();
  }
}, false); // Ctrl + S capture
```

2. Warn if user attempts to navigate away from `<form>` after changes

| **HTML** :
```html
<form method="get" onsubmit="offNavWarn();">
  <input type="text" name="something" onchange="onNavWarn();" onkeyup="onNavWarn();">
  <input type="submit" id="send_form" value="Send">
</form>
```

| **JavaScript** :
```js
function onNavWarn() {
  window.onbeforeunload = function() {
  return true;
  };
}
function offNavWarn() {
  window.onbeforeunload = null;
}
```

3. Update HTML to disappearing text with variables in the function

| **CSS** :
```css
@-webkit-keyframes fadeOut {
  0% { opacity: 1;}
  99% { opacity: 0.01;width: 100%; height: 100%;}
  100% { opacity: 0;width: 0; height: 0;}
}
@keyframes fadeOut {
  0% { opacity: 1;}
  99% { opacity: 0.01;width: 100%; height: 100%;}
  100% { opacity: 0;width: 0; height: 0;}
}
.hidenote {
  -webkit-animation: fadeOut 8s;
  animation: fadeOut 8s;
  animation-fill-mode: forwards;
}
```

| **HTML** :
```html
<button type="button" onclick="hideShow();">Hide show</button>
<span id="hideme" style="display: inline;">I want to hide.</span>
```

| **JavaScript** :
```js
function showNote(elemID, jsNote) {
  document.getElementById(elemID).innerHTML = '<span class="hidenote">'+jsNote+'</span>';
}
```

4. Send an alert to the browser

| **HTML** :
```html
<button type="button" onclick="showAlert();">Alert me</button>
```

| **JavaScript** :
```js
function showAlert() {
  window.alert("Consider yourself alerted!");
}
```

5. Hide/show by changing `display:` to `inline`/`none`

| **HTML** :
```html
<button type="button" onclick="hideShow();">Hide show</button>
<span id="hideme" style="display: inline;">I want to hide.</span>
```

| **JavaScript** :
```js
function hideShow() {
  if (document.getElementById("hideme").style.display === "inline") {
    document.getElementById("hideme").style.display = "none";
  } else {
    document.getElementById("hideme").style.display = "inline";
  }
}
```

## Try:

| **1** :$

```console
git clone https://github.com/inkVerb/HTML-CSS-JS
```

| **2** :$

```console
cd HTML-CSS-JS
```

| **3** :$

```console
gedit naked-sample.html styled-sample.html style.css scripts.js &
```

| **4** :$

```console
firefox naked-sample.html
```

*Use Ctrl + Shift + C in browser to see the developer view*

| **5** :$

```console
firefox styled-sample.html
```


*Use Ctrl + Shift + C in browser to see the developer view*

*Note "`<pre>prePREpre</pre>`" gets cut and hangs below its `<div>` because of fixed sizes and margins*

*Click: "Click me" then "Push"*

*Note the new address in the web browser*

| **6** :$

```console
javascript.html`

**First:** `<form>` hotkey and nav-away warning

*Type in the empty field, then click the browser's "Reload" or "Back" button*

*Note the message*

*Press "Crtl + S" and/or click "Send"*

*Note the `?g=...` in the browser address bar, "Ctrl + S" does the same as clicking "Send"*

**Second:** alert and update DOM

*Click other buttons in the lower half of the page*

*Note how the changes related between HTML and JavaScript*
