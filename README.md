# udacity-front-end-web-development

## Intro to HTML

* Fundamintals and building blocks, first HTML then css 
* We need to create layout and distribute component over it
* What is HTML and what it stands for?
* HTML is the basics, it is what you need to build a webpage.
* Hypertext -> http you see at start of URL
* Markup Language is a sequence of tags not a programing language.
* Why learn it? because it is the standard way to build a web page, combine it with css and js and you will have all you need.
* HTML Analogy is bones/skeleton, css is the cloths, js is the brain send the funcitonality.
* HTML is foundation, CSS is the style, js is functionality and behaviour.

### Text Elements

* There are alot of ways to express it we can use h1, p , div
* Block elements, p , ul, ol, h1, article, section, blockquote, divide elements into blocks
* Inline elements, a, em , stong is meant to differentiate part of text, used for single or few words.
* elements have atrributes that has value inside tag.
* span is used to wrap group of text usually for styling purpose

### HTML Lists

* Lists are every wehere in our world
* we have order and unorder list
* order has hirearchy , unorder dosne't

### Attributes

* Provide additional info about the tag.
* id, src, href
* img have width and height attributes
* img is self closing tag
* links a contains href, user it to navigate within the page, within the website, to another website
* use target attribute with a to specify where to open the linked document
* specify the rel attribute for the relationship between the current and linked document
* <a href="https://thelabradorclub.com" rel="noopener" target="_blank"
  >Join The Labrador Retriever Club</a>
* comment <!- ->
* https://developer.mozilla.org/en-US/docs/Web/HTML/Element

### The DOM

* Document Object Model, tree with nodes, it starts with a single parent item html then we go drill down.
* head tag is metaphor, metadata info about the page
* title tag inside head
* header for logo, nav for navigation, h1 for title, article for main content, footer for bottom of page, aside for side

### Forms

* form for collecting information, collecting input from the users
* text input, text areas, radi buttons, checkbox, dropdown, buttons
* <!-- A text input -->
<input type="text" />
<!-- A checkbox -->
<input type="checkbox" />
<!-- A radio button -->
<input type="radio" />
* fieldset tag, legend, checked
* <label for="color-select">Choose a color:</label>

<select id="color-select">
  <option value="">--Please choose an option--</option>
  <option value="blue">Blue</option>
  <option value="red">Red</option>
  <option value="green">Green</option>
  <option value="yellow">Yellow</option>
  <option value="orange">Orange</option>
  <option value="pink">Pink</option>
</select>
* <label for="learn">What do you hope to learn today?</label>

<textarea id="learn" name="learn" rows="5" cols="30">
I hope to learn about...
</textarea>

### Debugging

* Missing closing tags
* qutation errors

## Java script and DOm

### Document Object Model

- HTML and css are static, js can control them and make it dynamic
- DOM,  Modifying page, browser event and performance

### DOM
- document.getElementById('footer') not document.getElementById('#footer')
- Multi select .getElementByClassName or ByTagName
- The return of multi is not array it is html collection
- $0
- .querySelector() return first single element
- .querySelectorAll()
- Interface Node, Element

### Creating content with JS
- JS DOM delete, create and manipulate
- .innerHTML, textContent, innerText
- innertHTML property exists in any Element and it is responsible of element full html tags and it returns a string.
- inner select the inner of the tag
- outerHTML select the tag it self
- textContent only display the text content
- innerText dosen't show hidden, it shows what you see visually
- x = document.createElement('span')
- x.textContent = 'adsfasdf'
- .appendChild() it needs an element
- 
- const myPara = document.createElement('p');
const textOfParagraph = document.createTextNode('I am the text for the paragraph!');

myPara.appendChild(textOfParagraph);
document.body.appendChild(myPara);

SAME AS

const myPara = document.createElement('p');

myPara.textContent = 'I am the text for the paragraph!';
document.body.appendChild(myPara);
- appendChild moves the element from its current position to new one
- .insertAdjacentHTML() two argument the location of the HTML , the HTML text that is going to be inserted
<!-- beforebegin -->
<p>
    <!-- afterbegin -->
    Existing text/HTML content
    <!-- beforeend -->
</p>
<!-- afterend -->

- .removeChild() | 

const mainHeading = document.querySelector('h1');

mainHeading.parentElement.removeChild(mainHeading);

