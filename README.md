# EX01 Developing a Simple Webserver
## Date:14/03/2024

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
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>TOP SOFTWARE COMPANIES IN REVENUE</title>
</head>
<body>
<h1>Welcome<h1>
    <center><h1>TOP SOFTWARE COMPANIES BY REVENUE</h>
    <hr>
    <table border="10" cellspacing="20" height="100" width="75">
        <tr align="center">
            <th bgcolor="yellow">Comapny Name</th>
            <th bgcolor="yellow">Revenue</th>
            <th bgcolor="yellow">Net Income</th>
            <th bgcolor="yellow">Market Cap</th>
            <th bgcolor="yellow">Exchange</th>
            <th bgcolor="yellow">1yr Trailing Return</th>
        </tr>
        <tr align="center">
            <th bgcolor="yellow">Microsoft</th>
            <td bgcolor="cyan">$203 billion</td>
            <td bgcolor="cyan">70 billion</td>
            <td bgcolor="cyan">1.82 trillion</td>
            <td bgcolor="cyan">NASDAQ</td>
            <td bgcolor="cyan">-24.61%</td>
        </tr>
        <tr align="center">
            <th bgcolor="yellow">Oracle</th>
            <td bgcolor="cyan">$46 billion</td>
            <td bgcolor="cyan">$8.80 billion</td>
            <td bgcolor="cyan">$219 billion</td>
            <td bgcolor="cyan">NYS Exchange</td>
            <td bgcolor="cyan">-9.39</td>
        </tr>
        <tr align="center">
            <th bgcolor="yellow">SAP SE</th>
            <td bgcolor="cyan">$33 billion</td>
            <td bgcolor="cyan">$3.52 billion</td>
            <td bgcolor="cyan">122.57 billion</td>
            <td bgcolor="cyan">NYS Exchange</td>
            <td bgcolor="cyan">-22.08%</td>
        </tr>
        <tr align="center">
            <th bgcolor="yellow">Saleforce.Inc</th>
            <td bgcolor="cyan">$30 billion</td>
            <td bgcolor="cyan">$278 billion</td>
            <td bgcolor="cyan">$130 billion</td>
            <td bgcolor="cyan">NYS Exchange</td>
            <td bgcolor="cyan">-48.41%</td>
        </tr>
        <tr align="center">
            <th bgcolor="yellow">Abode Inc</th>
            <td bgcolor="cyan">$17.67 billion</td>
            <td bgcolor="cyan">$4.7 billion</td>
            <td bgcolor="cyan">$158 billion billion</td>
            <td bgcolor="cyan">NASDAQ</td>
            <td bgcolor="cyan">-38.77%</td>
        </tr>
    </table>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```

## OUTPUT:
![Screenshot 2024-03-15 101238](https://github.com/Narasimhan05/simplewebserver/assets/132819871/f2d3ecd1-c190-4f38-9ab3-68a007e7d376)

![Screenshot 2024-03-15 101217](https://github.com/Narasimhan05/simplewebserver/assets/132819871/5d3c2ee6-5353-475c-98b5-43c71ffe9965)

## RESULT:
The program for implementing simple webserver is executed successfully.
