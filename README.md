# HTTP Request–Response Cycle (GA)

## Start Every Coding Lab Ritual
- Create a fresh folder for the lab
- Initialize git
- Create README early
- Commit small wins often (one concept group per commit)
- Push to GitHub so progress is safe

## Key Vocabulary
- **Client**: the browser (Chrome/Safari)
- **Server**: the computer that receives requests and sends responses
- **HTTP**: rules for how clients and servers communicate
- **Request**: message sent from client to server
- **Response**: message sent back from server to client

## Concepts: What is HTTP?

HTTP (Hypertext Transfer Protocol) is a set of rules that defines how a browser
(client) communicates with a server.

- The browser sends a request
- The server sends back a response
- Each request–response pair is independent

### Stateless
HTTP is stateless, which means the server does not remember previous requests.

- After the server sends a response, the interaction ends
- Each new request is treated as if it is the first time
- Any “memory” (logins, carts, preferences) must be added separately (e.g., cookies or sessions)

## Fundamentals: Request–Response Cycle

The HTTP request–response cycle describes how communication on the web works.

1. A user performs an action (typing a URL, clicking a link, submitting a form)
2. The browser (client) sends an HTTP request to a server
3. The server receives the request and processes it
4. The server sends an HTTP response back to the browser
5. The browser displays the result to the user

Each request–response interaction is separate.
After the response is sent, the connection ends.


## HTTP Methods
HTTP methods describe the action a client wants to perform on a server.

- **GET**: Retrieve data from the server (does not change data)
- **POST**: Create new data on the server
- **PUT**: Update existing data on the server
- **DELETE**: Remove data from the server

The method communicates intent, not just the resource being accessed.

## Anatomy of HTTP Request/Response Messages

Every HTTP request and response follows the same structure, in this order:

1. **Start line**
   - Requests: includes the HTTP method and path (e.g., GET /tacos)
   - Responses: includes the status code (e.g., 200 OK)

2. **Headers**
   - Provide extra information about the request or response
   - Examples: Content-Type, Host

3. **Empty line**
   - Separates headers from the body

4. **Body**
   - Contains the actual data (HTML, JSON, text)
   - If there is data, it lives in the body

### HTTP Status Codes

Status codes appear in the response start line and describe the result of a request.

- **1xx**: Informational — request received, still processing
- **2xx**: Success — the request worked
- **3xx**: Redirect — the client should go somewhere else
- **4xx**: Client error — the request was incorrect (e.g., 404 Not Found)
- **5xx**: Server error — the server failed to handle the request (e.g., 500)


## Sending HTTP Requests From the Browser

Browsers send HTTP requests whenever a user interacts with a webpage.

### URL Anatomy

A URL tells the browser where to go and what to ask for.

Example:
https://localhost:3000/tacos?spicy=true

- **Protocol**: how to communicate (http or https)
- **Host**: which computer to talk to (e.g., localhost)
- **Port**: which door on that computer (e.g., 3000)
- **Path**: which resource is requested (e.g., /tacos)
- **Query parameters**: extra instructions (e.g., spicy=true)

### Browser Behavior

- Typing a URL or clicking a link sends a GET request
- Loading one webpage usually triggers many HTTP requests
  (HTML, CSS, JavaScript, images, fonts)
- `localhost` refers to the user’s own computer during development


## Cheat Sheet

### HTTP Basics
- HTTP is a set of rules for communication between a browser (client) and a server
- Communication happens in a request → response cycle
- HTTP is stateless: the server does not remember past requests

### Request–Response Cycle
1. Browser sends a request
2. Server processes it
3. Server sends a response
4. Connection ends

### HTTP Methods
- GET: retrieve data
- POST: create data
- PUT: update data
- DELETE: remove data

### HTTP Message Structure
1. Start line
2. Headers
3. Empty line
4. Body (actual data)

### Status Codes
- 1xx: informational
- 2xx: success
- 3xx: redirect
- 4xx: client error
- 5xx: server error

### URL Anatomy
- Protocol: how to communicate (http/https)
- Host: which computer
- Port: which door on that computer
- Path: what resource is requested
- Query parameters: extra instructions

## Laminated Checklist

### Before Sending a Request
- Do I know which server I’m talking to (host)?
- Do I know which resource I’m asking for (path)?
- Am I using the correct HTTP method (GET, POST, etc.)?
- Do I need query parameters (filters, options)?

### When Reading a Response
- Check the status code first (2xx, 4xx, 5xx)
- Look at headers for metadata (content type, length)
- Read the body for the actual data

### Mental Model Check
- Client always initiates the request
- Server always responds
- One request → one response
- HTTP itself is stateless

