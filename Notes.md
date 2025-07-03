# Front End Learning
## Notes taken during the training

//```Javascript tells VS Code in the markdown file we're working in JS until told otherwise


- HTML - Hypertext Markup Language, is the structure of a website/page
- CSS - color & styling
- JS allows programs to run embedded
- URL - Uniform Resource Locator
- Hypertext transfer protocol, http/https is the protocol
- www.example.com is the domain name
- /index.html is the file path

There are different types of hosting, shared, virtual private, dedicated, and cloud, for renting domain names, hosting websites, and email servers.
  - Shared hosting is where a user pays for space on a server that is shared with many other users. This means you're sharing resources (CPU, memory, bandwidth, etc.) with many other users. This is great for small websites with low traffic.
  - VPS, virtual private servers, solves the above problem for larger sites with higher traffic by providing defined infrastructure for each instance of a server.
  - Dedicated hosting is when a hardware server is solely dedicated to one website
  - Cloud hosting is shared hosting by over multiple servers both physical and virtual - this is the most scalable option so many pay as you go plan are popular

Internet protocols (IP)
   - TCP - Transmission Control Protocol requires a handshake from both the client and server so that data transfers intact and in order, but at the cost of the handshake delay
   - UDP - User Datagram Protocol doesn't require a handshake and therefore is faster at moving data, but data can arrive corrupt or not in order, this is the protocol for phone calls or streaming
   - HTTP - hyertext transfer protocol - a protocol followed for transfering web pages, images, and other files

An HTTP request looks like this
### Header
```html
    GET / HTTP/1.1
    Host: developer.mozilla.org
    Accept-Language: en
```
  - GET is the method (Most common are GET (retrieve from server), POST (send to server), PUT (Updates server), and DELETE (removes from server))
  - / is the path (where the resource you want to touch is located on the server)
  - HTTP/1.1 is the version (there are multiple versions but 1.1 and 2.0 are the most common currently)
  - Host: developer.mozilla.org and Accept-Language: en are headers

An HTTP response looks like this

### Header
```html
    HTTP/1.1 200 OK
    Date: Sat, 09 Oct 2010 14:28:02 GMT
    Server: Apache
    Last-Modified: Tue, 01 Dec 2009 20:18:22 GMT
    ETag: "51142bc1-7449-479b075b2891b"
    Accept-Ranges: bytes
    Content-Length: 29769
    Content-Type: text/html
```
### Body
```html
    <html>
    <body>
    <p>Hello world!</p>
    </body>
    </html>
```
  - 200 OK is a status code and message, codes are in the ranges of 100 to 599 and grouped by purpose, famous example is 404 page not found
    - 100-199 is Informational
    - 200-299 is Successful
    - 300-399 is Redirection
    - 400-499 is Client error
    - 500-599 is Server error

HTTPS is a secure version of HTTP, used for the transfering of private data like health and credit card info using encryption

### HTML Tags and elements
  - Sir Tim Berners-Lee wanted to share info to his friends and colleauges around the world, this started the creation of HTML
  - The very first webpage was created in 1989 by Sir Berners-Lee
  - He worked at the European organization for Nuclear Research (CERN)
  - The first version of HTML, web browser, and web server were released in 1991
  - Hypertext is text that contains links to other text
  - Markup refers to tags and elements used within a document
  - HTML is basically a text file with a specific structure that consists of elements and tags
  - HTML elements consist of
    - Opening tag in angle brackets `<p>` followed by a closing tag also in angle brackets `</p>`
    - Between the tags will usually contain content, for example

      `<p>This is a <i>paragraph</i></p>`

      Which results into
      <p>This is a <i>paragraph</i></p>

  - Elements can also be empty, or self closing, which doesn't need a closing tag, for example

      `<p>This is a <br>paragraph</p>`

      Results into

      <p>This is a <br>paragraph</p>

  - HTML standards - rules and structures in HTML specification maintained by the World Wide Web Consortium (W3C)
  - The current version of HTML is HTML5
  - HTML documents are text documents containing simple webpage formatting
  - Here is an example of a standard HTML structure:

```html
<!DOCTYPE html> <!-- This tells the webbrowser it's an html doc -->
<html> <!-- html tag to start, aka html root element -->
  <head> <!-- first of two main elements for webpage, nothing inside head element is displayed on the page on the webbroswer, this is where metadata is placed -->
      <title>Little Lemon</title> <!-- metadata for the page, can also link to CSS files, description of the webpage, keywords for search engines, and author of the webpage-->
  </head>
  <body> <!-- second of two main elements for webpage, here is where content of webpage goes, such as headings, paragraphs, images, and videos -->
    <h1>Our Menu</h1> <!-- Main heading -->
    <h2>Falafel</h2> <!-- Sub Heading #1 -->
    <p>Chickpea, herbs, and spices.</p> <!-- Paragraph information below SubHeading #1-->
    <h2>Pasta Salad</h2> <!-- Sub Heading #2 -->
    <P>Lettuce, vegetables, and mozzarella</p> <!--Paragraph info below SubHeading #2 -->
  </body>
</html>
```
- There are many tags available in HTML:
  - headings `<h1></h1>`
  - paragraphs `<p></p>`
  - line breaks `<br> or <br/>`
  - strong `<strong></strong>` which can be used to indicate that a range of text has imporance, makes the text appear bold
  - bold `<b></b>`
  - emphasis `<em></em>` is used to indicate a range of text is important, makes the text appear italisized
  - italics `<i></i>` used around technical terms, titles, thoughts or phrases from another language, etc.
  - unordered lists `<ul></ul>` with `<li></li>` Makes a bulleted outline list
    ```html
    <ul>
      <li>Tea</li>
      <li>Sugar</li>
      <li>Milk</li>
    </ul>
    ```
  - ordered lists `<ol></ol>` with `<li></li>` Makes a numbered outline list
    ```html
    <ol>
      <li>Rocky I</li>
      <li>Rocky II</li>
      <li>Rocky III</li>
    </ol>
    ```
  - You can change the type of bullet used in outlines depending on the CSS library you include.
    - For example, Google's Tailwind CSS allows you to change to lower case or upper case letters, or even Roman numerals
  ```html
          <h2 class="text-2xl font-semibold mb-3">Ordered List with Different Type (`<ol type="a">`)</h2>
        <!--
            You can change the type of marker for ordered lists using the 'type' attribute.
            'type="a"' for lowercase letters, 'type="A"' for uppercase letters,
            'type="i"' for lowercase Roman numerals, 'type="I"' for uppercase Roman numerals.
        -->
        <ol type="a" class="list-lower-alpha"> <!-- 'list-lower-alpha' is a Tailwind class for lowercase letters -->
            <li>Item A</li>
            <li>Item B</li>
            <li>Item C</li>
            <li>Item D</li>
        </ol>
  ```
  - Div tags define a content division in an HTML document.
    - It acts as a generic container and has no effect on the content unless it is styled by CSS.
    ```html
    <div>
     <p>This is a paragraph inside a div</p>
    </div>
    ```
  - It can be nested inside other elements:
    ```html
    <div>
    <div>
        <p>This is a paragraph inside a div that’s inside another div</p>
    </div>
    </div>
    ```
  - div's have no impact on content unless it's styled by CSS:
    ```html
        <style> <!-- This style is defining a boarder around each div, since there are two below this will result in a double boarder appearance around the paragraph -->
        div {
            border: 1px solid black;
            padding: 2px;
        }
      </style>
      <div>
        <div>
            <p>This is a paragraph inside stylized divs</p>
        </div>
      </div>
    ```
  - And comments can be left like so
    ```html
    <!-- This is a comment -->
    ```
  - anchor tags - create hyperlinks to link pages together
    - `<a href="example.html">Example Text</a>` a is the anchor tag, href is the hypertext reference, the file name of the linked page goes between the "", and in the tag body you can place any characters you want displayed for the link
  - image tags - this is to insert an image into a webpage
    - `<img src="Example.jpeg" width="240" height="135" alt="An example image">` img is the image tag, src is the source, the file name of the image goes between the "", the image file needs to be in the same folder location as the .html file referencing it for this example to work, width locks the image into a width of 240px, height locks the image into a height of 135px, the image will be resized to these dimensions, alt allows for short descriptions of the image for people who are using accessability readers.
  - table tags to create tables to display data
    ```html
    <table> <!-- table tag, start of table -->
      <tr>
        <th>Example Number</th> <!-- this is the table header tag and allows us to put in column titles in bold -->
        <th>Data Number</th>
      </tr>
      <tr> <!-- first table row -->
        <td>Example 1</td> <!-- table data -->
        <td>123</td> <!-- this will place this data to the right of Example 1 -->
      </tr>
      <tr> <!-- this starts a new row in the table -->
        <td>Example 2</td> <!-- table data -->
        <td>456</td>
      </tr>
    </table>
    ```
     Here is what the above would display as on a webbrowser.
    <table>
    <tr>
        <th>Example Number</th> 
        <th>Data Number</th>
      </tr>
      <tr>
        <td>Example 1</td>
        <td>123</td>
      </tr>
      <tr>
        <td>Example 2</td>
        <td>456</td>
      <tr>
    </table>
  - forms - `<form></form>` - allows users to input data that is then sent via http
    - the action tag within the form directs the data entered in the form where it is supposed to go

      `<form action="/registration" method="POST">`
    - when action is not specified it submits the request to the same path as the current webpage
    - label titles the input field created in the next step

      `<label for="username">Username:</label><br>`
    - input type adds fields the user can enter data into

      `<imput type="text" name="username">` this is a simple text input box.
      - This, however, only allows for single line tet input
      - for multiple lines use
      `<textareaname="multiline" rows="5"></textarea>`
    - html has a masking input type for use with sensative data, such as passwords
    

      `<label for="password">Password:</label><br>`

      `<input type="password" />`
    - submit buttons can be created

      `<input type="submit" />`
    - checkboxes can be created

      `<input type="checkbox" name="Checkbox 1" value="Yes" />`

      `<label for="Checkbox 1">Check here for yes.</label><br>`
    - Can also make radio button selections

      `input type="radio" name="right" value="Right" />`

      `label for="right"> I am right-handed.</label><br>`

      `input type="radio" name="left" value="Left" />`

      `label for="left"> I am left-handed.</label><br>`
    - other form types:
    
      `<input type="number" name="age" />`

      `<input type="email" name="email" />`

      `<input type="file" name="file" />`
  
- Another type of input that doesn't use the input tag is a dropdown list, it uses the select and option tags

  ```html
  <select name='food">
    <option value="chocolate">Chocolate</option>
    <option value="ice cream">Ice Cream</option>
  </select>
  ```

- To allow users to log in, like posts, or get notifications they need to be able to interact with items on the webpage, like react icons or comment button.
  - This is where **Document Object Model (DOM)** comes into play
  - When a user's web browser receives an HTML page it constructs a DOM to represent it
  - DOMs are a tree structure of objects
  - The DOM has a series of objects, each representing a single HTML element
    - The root of the DOM is the HTML object
    - the HTML object contains the `<head>` and `<body>` objects
    - The `<head>` object contains the `<title>` object which contains its `<text>` objects
    - The `<body>` object contains its `<div>` objects which will contain its `<h1>` and `<text>` objects, and so on, until a tree structure is formed which in its entirety is the DOM
  - The DOM allows you to update all HTML elements on a web page.
  - We use Javascript to access objects in the DOM to make them dynamic.
  - Common DOM and Javascript uses include:
    - Mouse hover, click, animate through libraries and frameworks
      - One of these libraries is the **REACT** library

- **Accessibility**
  - Practices that allow everyone can enjoy the websites, including those with disabilities
  - **W3C Web Accessibilities Initiative (WAI)** was launched in 1997
  - Web accessibility: allows people with disabilities to understand, navigate and interact with websites.
    - This includes all disabilities: visual, audio, cognitive, physical, and speech.
  - There are specifications and supporting resrouces:
    - International standards which are becoming a requirement in many industries
    - 2016 the EU approved the **Web Accessibility Directive (WAD)** which requires websites and mobile apps of public section bodies to be accessible to those with disabilities
  - Those with disabilities use tools to help them understand webpages:
    - Screen reader software reads what's happening on the page
    - Speech recognition software turns spoken words into commands or notate into text
    - Subtitles and video scripts
  - Using the correct HTML syntax like proper tags makes it easier for assistive tech to interpret whats on the screen
  - Really detailed websites can be very complex and still difficult for assistive tech to interpret so the WAI is developing the **Accessible Rich Internet Application (ARIA)** specification which outlines specific techniques to improve accessibility in complex web apps

### Frameworks and libraries
  - These are tools that devs use to make new software
  - Many devs use the terms interchangeably, but they are different
    - Libraries are reusable pieces of code that has a specific functionality
    - For example, if you're writing a website where a use can create a login, you might incorporate a step where the email the user inputs needs to be validated. There are half a dozen specs used for validating an email, instead of reading the specs and writing your own code, use code from a library.
    - Frameworks provide structure for a dev to work with. Example frameworks are Express, Django, ASP.NET, Rails, and Springs for web applications.
    - Most frameworks use many libraries, and the devs leave it up to the framework on which library to call for certain tasks
    - Frameworks force structure and can reduce dev time and have best practices, but sometimes the structure can be constraining and there can be compatibility issues if you want to use a library that the framework doesn't work with
    - If no framework is utilized, the dev will have to determine which libraries to use through the entire process, which gives the dev flexibility, but then also can incorporate compatibility issues if two or more libraries are in conflict

### APIs and Services
  - Application Programming Interface
  - It's a service, application, or interface offering advanced functionality with simple syntax
  - Common APIs include: browser, REST, and sensor-based
  - APIs are the bridge between different components or systems (aka gateway, middleware)
  - Browser/Web APIs - extend the functionality of the web browser by introducing new services
    - For example, the DOM API turns the html doc into a tree of nodes represented as JS objects
    - The geolocation API returns coordinates of where the browser is located
    - Fetch API fetches data
    - Canvas API draws graphics
    - History API keeps history
    - Web Storage API creates client side storage
  - Sensor-Based API - This is what IoT (Internet of Things) is based on
    - Physical sensors that are interconnected by communicating and tracking each other through the sensor-based API
  - RESTful API - provides data for popular web and mobile apps
    - A set of principles used to build highly efficient APIs
    - These are primarily used to send and retreive data from a centralized database efficiently
    - For web devs, this is the most common data API
    - A web server that provides responses to requests
    - These APIs use an endpoint like the following:

      `https://example.com/?t=info` Here the `?t=info` section of the URL is used to specify how different resources can be accessed
    
    - This is built into the URL. One the endpoint is hit, the API performed whatever server-side processing is needed to build the response.
    - Two common responses are full webpages and a data form based on JS called JSON

### IDE - Integrated Development Environment
  - This is the tool (software) used by devs to write their code
  - Some are specific to one programming language, others support many
  - IDEs have syntax highlighting to help developers differentiate keywords
  - Error highlighting also is available
  - Autocomplete is also incorporated while you're typing
  - Intellisense can detect functions and variables and make suggestions as you're writing
  - Refactoring is something else IDEs can do. Because IDEs understand your code, they can make suggestions on how to change it. When a variable or name of a function needs to be renamed, making sure it's consistantly renamed through the whole code and other files is called refactoring.
    - In VS Code, just right click on the variable or function name and select rename symbol

### CSS
  - Selecting and styling
  - CSS tells the web browser how to display the HTML elements on screen
  - There are five elements in CSS (CSS rule)
    - selector
    - declaration block { }
      - declaration
        - value
        - property

      ```css
      p {            /* the p is the seclector, indicates which HTML element you want to style */
        color: blue;  /* between the {} is the declaration block with the style declarations made of the value and its property */
      }
      ```
        - Each declaration block is made up of two parts: a property and a value
      `color: blue;`
        - Here "color" is the property
        - "blue" is the value
        - Because this declaration block is assigned to the `<p>` element, all `<p>` elements on the associated HTML page will be blue
    - There are different types of selectors
      - Element selectors like `p` or `h1`
      - ID selectors like `#title` or `#header1` when you want to make an exception to a single element
      - Class selectors like `.navigation` or `.footer` which can be assigned to all elements assigned to that class through
        ```html
        <a class="navigation">Go Back</a>
        <p class="navigation">Go Forward</p>
        ```
      - Can get more specific by selecting elements with a class selector

        *HTML*
        ```html
        <p class="introduction"></p>
        ```
        *CSS*
        ```css
        p.introduction {
          margin: 2px;
        }
        ```
      - **Descendant selectors** can be used to select HTML elements that are contained with in another selector

        *HTML*
        ```html
        <div id="blog">
          <h1>Latest News</h1>
          <div>
           <h1>Today's Weather</h1>
           <p>The weather will be sunny</p>
        </div>
        <p>Subscribe for more news</p>
        </div>
        <div>
          <h1>Archives</h1>
        </div>
        ```
      
        *CSS*
          ```css
          /* This rule will only apply to the h1 in ID blog, and not h1 in the next div container "Archives" */
          #blog h1 {
            color: blue;
          }
          ```
        - Multiple descendants can also be selected. For example, to select all `h1` elements that are descendants of `div` elements which are descendants of the `blog` elemeent, the selector is specified as follows:
          ```css
          #blog div h1 {
            color: blue;
          }
          ```
      - **Child selectors** are more specific than descendant selectors. They only select elements that are imediate descendants (childern) of a selector (the parent), for example this will style only the words "Latest News"

        *HTML*
        ```html
        <div id="blog">
          <h1>Latest News</h1>
          <div>
            <h1>Today's Weather</h1>
            <p>The weather will be sunny</p>
          </div>
          <p>Subscribe for more news</p>
        </div>
        ```
        *CSS*
        ```css
        #blog > h1 {
          color: blue;
        }
        ```
      - **:hover Pseudo-Class** is a special keyword which allows devs to select elements based on their state. This particular one allows you to style an element when a mouse cursor is hovered over that element (like hovering over a hyperlink)
        ```css
        a:hover {
          color: orange;
        }
        ```
      - There are many more selectors available for CSS styling
    - Text and color in CSS
      - In CSS v3 there are five main ways to reference a color:
        - RGB value
          - Red Green and Blue hues between 0 and 255 to change intensity
          - For example red would be 255, 0, 0
          - Black would be 0, 0, 0
          - White 255, 255, 255
          ```css
          p {
            color: rgb(255, 0, 0);
          }
          ```
        - RGBA value
          - Extension of RGB with an alpha (A) channel which reps opacity/transparancy
          ```css
          p {
            color: rgba(255, 0, 0, 0.8);
          }
          ```
        - HSL value
          - Newer color model
          - Hue (H), Saturation (S), and Lightness (L)
          - Take a rainbow and spin in a circle. The H is the degree of rotation determining color, S is the length of the radius determing the shade of the color, and L is how dark (black) or bright (white) you want that color/shade.
          ```css
          p {
            color: hsl(0, 100%, 50%);
          }
          ```
        - hex
          - This uses hexidecimal (hex) value with 16 digits: `0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F`.
          - Colors in hex start with a `#` followed by the RGB value in hexadecimal
          - For example, red would be `#FF0000`
        - predefined color names
          - There are 140 predefined color names in modern web browsers
          - common names include: black, silver, white, gray, red, purple, etc.
      - There are many ways to change how text is displayed using CSS
        - Color using the `color` property
        - Font and size uses the font-family property
          ```css
          p {
            font-family: "Courier New", monospace;
          }
          ```
        - Computers vary in what fonts they have installed, so it's recommended to incude several fonts when using the `font-family` property.
          - These are specified in fallback order, the first is the ideal font to use, the second is the first fall back option if the first font is not available, etc.
        - Size of font is specified like follows:
          ```css
          p {
            font-family: "Courier New", monospace;
            font-size: 12px;
          }
          ```
      - Text transformation if you want to ensure that text has the correct capitalization using `text-transform`
        ```css
        p {
          text-transform: uppercase;
        }
        ```
        - Values for `text-transform` include uppercase, lowercase, capitalize, and none (default)
      - Text decoration
        - `text-decoration` is useful to apply additional decoration to text like underline and strike-through
        ```css
        h1 { /* This is a solid red underline of 5px in thickness */
            text-decoration-line: underline;
            text-decoration-color: red;
            text-decoration-style: solid;
            text-decoration-thickness: 5px;
        }

        p { /* This is short-hand for the above */
          text-decoration: underline red solid 5px;
        }
        ```
        - Most common `text-decoration-line` values are underline, overline, line-through, and none
        - `text-decoration-style` values are solid (default), double, dotted, dashed, and wavy
      - Alignment within its content box is created using `text-align` for the property and `left, center, right, and justify` for the value. `Justify` will spread the text out so that every line of the text has the same width. Default is `left` for languages such as English, `right` for languages such as Arabic.
  - Box Model
    - Helps create an appealing layout of objects
    - Browser will dedicate a rectangle to each element to begin layout on the page
    - CSS rule are then tied to the boxes for styling
    - Every box model contains four parts listed here from inner to outermost:
      - Content
      - Padding
      - Border
      - Margin
    - Browsers will default the size of the content rectangle's height and width to the actual content but these dimentions can be controlled through styling/CSS rules
      - width: 1px;
      - min-width
      - max-width
      - height
      - min-height
      - max-height
    - Padding is the next layer up from the content rectangle
      - This size can be controlled by
      - padding-top
      - padding-bottom
      - padding-left
      - padding-right
      - shorthand: Padding: 4px 2px 1px 5px;
    - Border is the next layer above padding
      - borders can be set to solid, dashed, dotted, or double
      - border-width: thin, medium, or thick
      - shorthand: border-width: 2px 3px 1 px 4px;
    - Margins are the next layer above border
      - margin-top: 4px;
      - margin-bottom
      - margin-left
      - margin-right
      - shorthand: margin: 1px 2px 4px 5px;
  - Document flow: block vs. inline
    - Document flow is how the browser calculates where to display the content on the screen
    - Elements are organized in one of two catagories: block or inline
      - block occupies the full horizontal width of the screen and the vertical height of the content, each element ends on a new line, so the next block will appear below the first which results in a stack of blocked elements on the screen
        - block level elements include `<div>, <form>, <h1>, <h2>, <h3>, <h4>, and <h5>`
      - inline elements only occupy the width and height of their content and don't appear on a new line (hence "inline") 
        - inline elements include `<a>, <img>, <input>, <label>, <b>, <i>, <em>, and <span>`
      - element defaults of block or inline can be overwritten using CSS
        ```css
        #id {
          display: inline; /* or block */
        }
        ```
    - Alignment for elements is more complicated than text alignment
      - Center alignment is acheived through setting a width on the element and pushing its margins out to fill the remaining available space of the parent element.  
