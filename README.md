# Browser–Server Communication Using HTTP & HTTPS

## 1. Introduction

When you type a website address (URL) into a browser and press Enter, the browser communicates with a **web server** to fetch and display the requested content. This communication happens using **HTTP** or **HTTPS**, which are standard protocols of the web.

---

## 2. What is HTTP?

**HTTP (HyperText Transfer Protocol)** is a set of rules that defines how a browser (client) and a web server communicate.

- It is a **request–response** protocol
- The browser sends a request
- The server sends back a response (HTML, CSS, JS, images, data, etc.)
- HTTP is **stateless** (each request is independent)

### Example:

```
<http://example.com>

```

⚠️ Data sent using HTTP is **not encrypted**, so it is less secure.

---

## 3. What is HTTPS?

**HTTPS (HyperText Transfer Protocol Secure)** is the secure version of HTTP.

- Uses **SSL/TLS encryption**
- Protects data from hackers and eavesdropping
- Ensures **confidentiality, integrity, and authentication**

### Example:

```
<https://example.com>

```

🔒 Most modern websites use HTTPS for security.

---

## 4. URL Breakdown (Important)

A **URL (Uniform Resource Locator)** tells the browser where and how to access a resource.

### Example URL:

```
<https://www.example.com:443/path/page.html?user=akash&id=10#section1>

```

### Parts of a URL:

1. **Protocol (Scheme)**
    - `https://`
    - Defines the communication rules (HTTP or HTTPS)
2. **Domain Name (Host)**
    - `www.example.com`
    - Human-readable address of the server
3. **Port (Optional)**
    - `:443`
    - HTTP → 80, HTTPS → 443 (default)
4. **Path**
    - `/path/page.html`
    - Location of the resource on the server
5. **Query Parameters**
    - `?user=akash&id=10`
    - Used to send data to the server (key–value pairs)
6. **Fragment (Anchor)**
    - `#section1`
    - Used for internal page navigation (not sent to server)

---

## 5. Step-by-Step: How Browser Communicates with Server

### Step 1: User Enters URL

The user types a URL into the browser.

### Step 2: DNS Resolution

- Browser asks **DNS** to convert domain name into IP address
- Example:
    
    ```
    example.com → 93.184.216.34
    
    ```
    

### Step 3: TCP Connection

- Browser creates a TCP connection with the server
- HTTPS additionally performs **TLS Handshake**

### Step 4: HTTP/HTTPS Request

Browser sends a request:

```
GET /index.html HTTP/1.1
Host: example.com
User-Agent: Chrome

```

### Step 5: Server Processes Request

- Server finds the requested resource
- Runs backend logic (if needed)

### Step 6: HTTP/HTTPS Response

Server responds:

```
HTTP/1.1 200 OK
Content-Type: text/html

<html>...</html>

```

### Step 7: Browser Renders Page

- HTML is parsed
- CSS is applied
- JavaScript is executed
- Page is displayed to the user

---

## 6. HTTP vs HTTPS (Comparison)

| Feature | HTTP | HTTPS |
| --- | --- | --- |
| Security | ❌ Not secure | ✅ Secure |
| Encryption | ❌ No | ✅ Yes |
| Default Port | 80 | 443 |
| SEO Ranking | Lower | Higher |
| Trust | Low | High |

---

## 7. Common HTTP Methods

- **GET** → Request data
- **POST** → Send data
- **PUT** → Update data
- **DELETE** → Remove data


