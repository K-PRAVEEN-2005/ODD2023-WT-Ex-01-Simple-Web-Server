# Ex-01-Simple-Web-Server
## Date:

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:

```
content = """
<html>
<head>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h3>1.Django</h3>
<h3>2.MEAN Stack</h3>
<h3>3.React</h3>
</body>
</html>
"""
class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('Content-type','text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())


server_address = ('', 80)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```
## OUTPUT:
![web server](https://github.com/K-PRAVEEN-2005/ODD2023-WT-Ex-01-Simple-Web-Server/assets/145742724/034c4ead-94f7-42ef-9969-cb9e069113e7)


## RESULT:
The program for implementing simple webserver is executed successfully.
