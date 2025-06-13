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

Frameworks and libraries
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





  