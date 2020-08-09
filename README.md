functions are just values  
anonymous functions
# DOM
# (DOCUMENT OBJECT MODEL)

HTML and CSS lay out the foundation for us to work with
- Tree of nodes/elements created by the browser.
- javascript helps to read/write/modify that foundation to the DOM
- Object Oriented Representation
  
![](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn.tutsplus.com%2Fnet%2Fuploads%2Flegacy%2F216_dom%2Fimg%2Fdom_basic.png&f=1&nofb=1)

<hr>
<hr>

## SELECTOR


### console.dir()
#### shows us all of the different properties and methods attached to the document object.

- The Console method dir() displays an interactive list of the properties of the specified JavaScript object. The output is presented as a hierarchical listing with disclosure triangles that let you see the contents of child objects.

- In other words, `console.dir()` is the way to see all the properties of a specified JavaScript object in console by which the developer can easily get the properties of the object.

dev tool 
ctrl + option + i =  OPENS INSPECT PAGE IN BROWSER
f12 = OPENS INSPECT PAGE IN BROWSER
ctrl + shift + c = element selector
<hr>
<hr>


## Query Selector
## document.querySelector()

- document is based on the webpage it interacts with.
- can be used for id's, classes, tags.
- only grabs the first element
### Syntax
```javascript
document.querySelector(CSS selectors)
```

- takes in a string
- return one eelment
- search that document for that selector
- returns an object
- allows us to manipulate the document selector using Javascript Objects syntax.
- query the document for a  specific element
- document.querySelector()

<hr>
<hr>

link javascript file at the end of inside the body.

```javascript
    <script src ='./script.js'></script>
</body>
```

<hr>
<hr>

## querySelectorAll()
-   able to select multiple items unlike querySelector() which only selects one
-   returns an array-like structure

## Example querySelectorAll()
```javascript
const makeSelfBlue = function (event) {
    const itemClicked = event.target
    itemClicked.style.color = 'blue';
}


const allItems =  document.querySelectorAll('.item');
for (const item of allItems) {
    item.addEventListener('click', makeSelfBlue);
}
```

<hr>
<hr>

## Event Listeners Javascript
## addEventListener()

- flexible event model.
- can assign as many event listeners as you like to a particular event on a particular element.
- a way, using a callback functions, you tell me what element the user interacts with, how they interact with it, and what code should i run
- A listener refers to a function that is waiting to be run.
## Syntax :   addEventListener()
```javascript
target.addEventListener(event, function, useCapture);
```

##  Example :  addEventListener()

**Now, if you run the below example and click the button, both functions will be executed.**

```javascript
<button id="myBtn">Click Me</button>
 
<script>
// Defining custom functions
function firstFunction() {
    alert("The first function executed successfully!");
}
 
function secondFunction() {
    alert("The second function executed successfully");
}

// Selecting button element
var btn = document.getElementById("myBtn");
 
// Assigning event listeners to the button
btn.addEventListener("click", firstFunction);
btn.addEventListener("click", secondFunction);
</script>
```

## Adding Event Listeners for Different Event Types  
## Example  

```javascript
<button id="myBtn">Click Me</button>
 
<script>
// Selecting button element
var btn = document.getElementById("myBtn");
 
// Defining custom functions
function sayHello() {
    alert("Hi, how are you doing?");
}
 
function setHoverColor() {
    btn.style.background = "yellow";
}
 
function setNormalColor() {
    btn.style.background = "";
}
 
// Assigning event listeners to the button
btn.addEventListener("click", sayHello);
btn.addEventListener("mouseover", setHoverColor);
btn.addEventListener("mouseout", setNormalColor);
</script>
```
<hr>
<hr>

## Removing Event Listeners
- You can use the removeEventListener() method to remove an event listener that have been previously attached with the addEventListener(). Here's an example:

## Example
```javascript
<button id="myBtn">Click Me</button>
 
<script> 
// Defining function
function greetWorld() {
    alert("Hello World!");
}
 
// Selecting button element
var btn = document.getElementById("myBtn");
 
// Attaching event listener
btn.addEventListener("click", greetWorld);
 
// Removing event listener
btn.removeEventListener("click", greetWorld);
</script>  
```  
<hr>
<hr>





## Methods Learned in Week 12

### getElementById()
- Get the element with the specified ID:
  <hr>
  <hr>
### getElementByTagName

  <hr>
  <hr>

### Array.from()
- make a list into an array
  
    <hr>
  <hr>
## .target property 
- refers to what was clicked

    <hr>
  <hr>
## event
- the entire information and details on what occured while that click event happen, 
  
    <hr>
  <hr>
## forEach()
- takes in a function
- run the function on every element in the array for me

  <hr>
  <hr>
## toFFixed()

  <hr>
  <hr>

## resudce taekd  a nunch

  <hr>
  <hr>

## .classList
- DOMTokenList (an array-like property)
- bold
- array of string, bold, square, etx.

  <hr>
  <hr>


  
## .className

  <hr>
  <hr>

## Element.classList.add()
- adding a css class to that element

  <hr>
  <hr>

## Element.classList.remove()
- looks for class name that was added and remove it if it is there in the element

  <hr>
  <hr>

## Element.classList.toggle()
- looks if class name is there
- if it is there, it removes it.
- if it is not there, it adds it.

  <hr>
  <hr>


## .contains
-   classList's version of `.includes`.
-   does this tag contain the class 

  <hr>
  <hr>

## .replace
- looks for the first argument, and if it's there. replace it with second argument
- **syntax**
  ```javascript
  list1.replace('high-contrast', 'low-contrast')
  ```

## document.createElement()
## Example 
## Create a <button> button: </button> element 
```javascript
var btn = document.createElement("BUTTON");
```

  <hr>
  <hr>

## document.createElement 
- The createElement() method creates an Element Node with the specified name.
## Syntax:
```javascript
document.createElement(nodename)
```
## Example
### Create a <p> element and append it to a <div> element:

```javascript
var para = document.createElement("P");                 // Create a <p> element
para.innerHTML = "This is a paragraph.";                // Insert text
document.getElementById("myDIV").appendChild(para);     // Append <p> to <div> with id="myDIV"
```
<hr>
<hr>

## HTML DOM appendChild() Method
### The appendChild() method appends a node as the last child of a node.

## Example
### Append an item in a list:

```javascript
var node = document.createElement("LI");                 // Create a <li> node
var textnode = document.createTextNode("Water");         // Create a text node
node.appendChild(textnode);                              // Append the text to <li>
document.getElementById("myList").appendChild(node);     // Append <li> to <ul> with id="myList"
```
## Syntax
```javascript
node.appendChild(node)
```
<hr>
<hr>
