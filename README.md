# What is WebDriver and Selenium?

When it comes to testing, these two terms WebDriver and Selenium are interchangeably used to refer the automating the web application.

Technically, WebDriver is a standard, HTTP based API for interacting with a web browser. The standard is provided by W3C.

The W3C WebDriver API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser.

Most of the browser vendors implements the [W3C WebDriver standard](https://w3c.github.io/webdriver/webdriver-spec.html) (JSON wire protocol is _OBSOLETE_ now) as a standalone server.

-   Chrome:  [https://sites.google.com/a/chromium.org/chromedriver/downloads](https://sites.google.com/a/chromium.org/chromedriver/downloads)
-   Firefox:  [https://github.com/mozilla/geckodriver/releases](https://github.com/mozilla/geckodriver/releases)
-   Opera:  [https://github.com/operasoftware/operachromiumdriver/releases](https://github.com/operasoftware/operachromiumdriver/releases)
-   EDGE:  [https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/#downloads](https://developer.microsoft.com/en-us/microsoft-edge/tools/webdriver/#downloads)

#### Download ChromeDriver and PostMan
The first step is to [download](https://sites.google.com/a/chromium.org/chromedriver/downloads) the ChromeDriver executable from Google ChromeDriver Page. In my case, I’m using a Mac, so I download `chromedriver_mac64.zip`.

To interact with the API we need a tool that allows us to make HTTP requests. For that we need to download [Postman](https://www.getpostman.com/). So that you can send and receive API request from PostMan.

#### Testcase:
The testcase that we are going to automate as follows,

 1. Open the chrome browser
 2. Navigate to Google page
 3. Locate search text box
 4. Send as earch value
 5. Locate google search button
 6. Click on search button
 7. Quit driver

#### Start ChromeDriver on Terminal:
Extract the file and run it. You will be given the port on which the WebDriver API is exposed.

```
$ Downloads ./chromedriver 
Starting ChromeDriver 80.0.3987.106 (f68069574609230cf9b635cd784cfb1bf81bb53a-refs/branch-heads/3987@{#882}) on port 9515
Only local connections are allowed.
Please protect ports used by ChromeDriver and related test frameworks to prevent access by malicious code.
```
#### Open the chrome broswer:

The first step is to open the browser. This is done by creating a new session. To create a new session via the WebDriver API, we make a HTTP POST request to the  [`/session`](https://w3c.github.io/webdriver/#new-session)  endpoint. In addition, we need to define the type of browser we wish to open. This information is sent in a JSON object in the POST body.

















#### References:

 1. [https://www.erranderr.com/blog/webdriver-ontology.html](https://www.erranderr.com/blog/webdriver-ontology.html)
 2. [https://kobiton.com/selenium/w3c-webdriver-protocol/](https://kobiton.com/selenium/w3c-webdriver-protocol/)
