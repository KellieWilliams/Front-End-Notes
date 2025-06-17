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
  



### Frameworks and libraries
  - These are tools that devs use to make new software
  - Many devs use the terms interchangeably, but they are different
    - Libraries are reusable pieces of code that has a specific functionality
    - For example, if you're writing a website where a use can create a login, you might incorporate a step where the email the user inputs needs to be validated. There are half a dozen specs used for validating an email, instead of reading the specs and writing your own code, use code from a library.
    - Frameworks provide structure for a dev to work with. Example frameworks are Express, Django, ASP.NET, Rails, and Springs for web applications.
    - Most frameworks use many libraries, and the devs leave it up to the framework on which library to call for certain tasks
    - Frameworks force structure and can reduce dev time and have best practices, but sometimes the structure can be constraining and there can be compatibility issues if you want to use a library that the framework doesn't work with
    - If no framework is utilized, the dev will have to determine which libraries to use through the entire process, which gives the dev flexibility, but then also can incorporate compatibility issues if two or more libraries are in conflict

APIs and Services
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

IDE - Integrated Development Environment
  - This is the tool (software) used by devs to write their code
  - Some are specific to one programming language, others support many
  - IDEs have syntax highlighting to help developers differentiate keywords
  - Error highlighting also is available
  - Autocomplete is also incorporated while you're typing
  - Intellisense can detect functions and variables and make suggestions as you're writing
  - Refactoring is something else IDEs can do. Because IDEs understand your code, they can make suggestions on how to change it. When a variable or name of a function needs to be renamed, making sure it's consistantly renamed through the whole code and other files is called refactoring.
    - In VS Code, just right click on the variable or function name and select rename symbol

  