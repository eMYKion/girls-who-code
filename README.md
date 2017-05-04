# girls-who-code
An easy-to-follow three.js tutorial for learners of WebGL technology.
Used in a workshop for the [Girls Who Code](https://girlswhocode.com/) organization.
This tutorial contains code to render a spinning red cube, right on your webpage!

First create the two necessary files for this project: index.html and three.js.

# getting started with index.html
The browser of your choice will be used to render index.html, which sources the JavaScript library three.js. 
index.html is written in HTML format, or HyperText Markup Language, which contains a set of tags, for example:

`<tag></tag>`

Note that this shows a closed tag, with a proper ending. If another closed tag is put inside this tag (between the `<tag>` and `</tag>`),
it is called the child of this tag, and this tag is the parent. A parent tag can have multiple children or none. Notice how with these
simple rules, an HTML page can be depicted as an upside-down tree, where branches indicate children tags.

Standard boilerplate code for any HTML page is as follows:

```
<!DOCTYPE html>

<html>

  <head></head>
  
  <body></body>
  
</html>
```

The `<!DOCTYPE html>` is ignored by the browser when it renders the layout of the page since its tag name begins with an exclamation 
mark. This just tells the browser that the file type is an HTML page. In general, an HTML comment tag can be written as: 

`<!--this is a comment-->`

Notice that this HTML file has a root tag: namely, `<html>`. This contains metadata in the `<head></head>` tag. The `<body></body>` tag
contains all the visible/runnable content on your webpage.

To make a webpage title (this is what a search engine displays on your search results), simply put a `<title></title>` tag in the 
`<head></head>` tag. For this tutorial, we name our webpage "Spinning Cube":

```
<!DOCTYPE html>

<html>

  <head>
    <title>Spinning Cube</title>
  </head>
  
  <body></body>
  
</html>
```

If you opened this page with your browser, you will get a blank page, but the tab will say "Spinning Cube". Nifty eh?

Lastly, we are going to need a container for our rendering element which we will write in JavaScript later. You can think that this 
element will actually modify the pixels on your webpage.

Go ahead and add a `<div id="view"></div>` tag in the `<body></body>` tag. You can think that this means "division", and it is used to 
organize regions on a webpage. the `id="view"` snippet inside the first tag tells the browser that the name of this tag will be called 
"view". This will make it easier for JavaScript to manipulate tags of the document (webpage) by referencing them directly, as we will 
soon do. When naming tags, it is good practice to assign unique names (no duplicate `id`s allowed!).

Next, we are going to reference the three.js library with the `<script></script>` tag. It is okay to put this in the body, but you 
normally would reference libraries in the `<head></head>` tag. Remember that calling libraries must be done before your code that uses 
them, or you will get errors. Go ahead and put a  `<script src="./three.js"></script>` tag in the `<body></body>` tag. The 
`src="./three.js"` snippet tells the browser to look for a file called "three.js" in the same scope as the HTML file being rendered. 

Where is this file you ask? Great question! Go on over to the [official three.js GitHub repository](https://github.com/mrdoob/three.js/blob/dev/build/three.js) 
and copy the contents of three.js into a file called three.js next to your index.html file. This is a large file, so you can use the 
minified version, three.min.js, instead. Just remember to change the name referenced in the index.html file to match.

Since we are going to write our own JavaScript code, go ahead and put an empty `<script></script>` tag in the `<body></body>` tag. under the other body's other children tags.

Now you should have:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Spinning Cube</title>
  </head>
  
  <body>
    <div id="view"></div>
    <script src="./three.js"></script>
    <script></script>
    
  </body>
</html>
```

Great, now let's move on to writing JavaScript!

# Writing JavaScript

Since this tutorial is still under construction, go ahead and copy the contents of that "empty" `<script></script>` tag from the previous step from this project's index.html, and enter it into the `<script></script>` tag. Load the page, and you should see a spinning cube. If you cannot wait for this section to be written, there are hundreds of these kinds of tutorials elsewhere on the internet, such as [Aerotwist's three.js tutorial](https://aerotwist.com/tutorials/getting-started-with-three-js/). Enjoy!
