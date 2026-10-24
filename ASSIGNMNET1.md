<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>What Happens Between Typing a URL and Seeing the Page?</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f2f6fc;
            color: #263238;
            line-height: 1.7;
        }

        header {
            background: linear-gradient(135deg, #102a43, #176b87);
            color: white;
            text-align: center;
            padding: 45px 20px;
        }

        header h1 {
            font-size: 32px;
            margin-bottom: 12px;
        }

        header p {
            font-size: 17px;
        }

        nav {
            background-color: #0b1f33;
            padding: 14px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 15px;
            font-weight: bold;
        }

        nav a:hover {
            color: #64d8cb;
        }

        .container {
            width: 90%;
            max-width: 1000px;
            margin: 30px auto;
        }

        .section {
            background-color: white;
            padding: 25px;
            margin-bottom: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.07);
        }

        h2 {
            color: #176b87;
            margin-bottom: 15px;
            border-bottom: 2px solid #d7e9f0;
            padding-bottom: 8px;
        }

        .steps {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 18px;
        }

        .step {
            background-color: #f4f9fc;
            border-left: 5px solid #176b87;
            padding: 18px;
            border-radius: 8px;
        }

        .step h3 {
            color: #102a43;
            margin-bottom: 8px;
        }

        .number {
            display: inline-block;
            background-color: #176b87;
            color: white;
            padding: 3px 10px;
            border-radius: 50%;
            margin-right: 6px;
        }

        .flow {
            background-color: #e4f3f7;
            padding: 20px;
            text-align: center;
            border-radius: 10px;
            font-weight: bold;
            color: #102a43;
        }

        .arrow {
            color: #176b87;
            font-size: 24px;
            margin: 4px 0;
        }

        code {
            background-color: #e8edf2;
            padding: 3px 6px;
            border-radius: 4px;
            color: #b83250;
        }

        ul {
            padding-left: 25px;
        }

        footer {
            background-color: #102a43;
            color: white;
            text-align: center;
            padding: 20px;
            margin-top: 40px;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 25px;
            }

            nav a {
                display: inline-block;
                margin: 5px 8px;
            }

            .container {
                width: 94%;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>What Happens Between Typing a URL and Seeing the Page?</h1>
        <p>Understanding the Journey of a Web Request</p>
    </header>

    <nav>
        <a href="#introduction">Introduction</a>
        <a href="#process">Process</a>
        <a href="#flowchart">Flowchart</a>
        <a href="#conclusion">Conclusion</a>
    </nav>

    <main class="container">

        <section class="section" id="introduction">
            <h2>1. Introduction</h2>

            <p>
                Every time we type a website address into a browser and press
                Enter, several processes take place behind the scenes.
                The browser communicates with servers, receives website files,
                and converts them into a page that we can see and interact with.
            </p>

            <p>
                This assignment explains the complete process, from entering
                a URL to displaying the final webpage on the screen.
            </p>
        </section>

        <section class="section" id="process">
            <h2>2. Step-by-Step Process</h2>

            <div class="steps">

                <article class="step">
                    <h3><span class="number">1</span>Entering the URL</h3>
                    <p>
                        The user types a URL, such as
                        <code>https://example.com</code>, into the browser
                        and presses Enter.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">2</span>Browser Cache</h3>
                    <p>
                        The browser checks whether useful resources are
                        already stored in its cache. Cached resources may
                        reduce the need to download them again.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">3</span>DNS Lookup</h3>
                    <p>
                        The Domain Name System (DNS) translates the domain
                        name into an IP address so the browser can locate
                        the appropriate server. Cached DNS results may
                        avoid a new lookup.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">4</span>Connection Setup</h3>
                    <p>
                        The browser establishes a connection with the server.
                        HTTP/1.1 and HTTP/2 commonly use TCP, while HTTP/3
                        uses QUIC. HTTPS also establishes secure
                        cryptographic protection.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">5</span>HTTP Request</h3>
                    <p>
                        The browser sends an HTTP request asking for a
                        resource. For example, a request may use
                        <code>GET /index.html</code>.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">6</span>Server Response</h3>
                    <p>
                        The server processes the request and sends an HTTP
                        response containing a status code, headers, and
                        usually the requested content. For example,
                        <code>200 OK</code> indicates success.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">7</span>HTML and DOM</h3>
                    <p>
                        The browser parses the HTML document and builds
                        the Document Object Model (DOM), which represents
                        the structure of the webpage.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">8</span>Loading Resources</h3>
                    <p>
                        The browser discovers linked CSS files, JavaScript,
                        images, fonts, and other resources. It requests
                        them when necessary.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">9</span>CSSOM and Rendering</h3>
                    <p>
                        The browser parses CSS into the CSS Object Model
                        (CSSOM). It combines the relevant DOM and CSS
                        information to determine styles and layout.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">10</span>Layout and Painting</h3>
                    <p>
                        The browser calculates element positions and sizes,
                        paints visual content, and composites the layers
                        to display the page on the screen.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">11</span>JavaScript Execution</h3>
                    <p>
                        JavaScript runs according to the document's scripts
                        and loading rules. It can respond to user actions,
                        change page content, and request additional data.
                    </p>
                </article>

                <article class="step">
                    <h3><span class="number">12</span>Final Webpage</h3>
                    <p>
                        The webpage becomes visible and interactive.
                        Additional resources or scripts may continue
                        loading, and the page can update dynamically.
                    </p>
                </article>

            </div>
        </section>

        <section class="section" id="flowchart">
            <h2>3. Flowchart of the Process</h2>

            <div class="flow">
                User Enters a URL
                <div class="arrow">↓</div>

                Browser Checks Cache
                <div class="arrow">↓</div>

                DNS Resolves Domain Name
                <div class="arrow">↓</div>

                Connection and Secure Setup
                <div class="arrow">↓</div>

                Browser Sends HTTP Request
                <div class="arrow">↓</div>

                Server Sends HTTP Response
                <div class="arrow">↓</div>

                Browser Parses HTML and CSS
                <div class="arrow">↓</div>

                DOM, CSSOM, Layout and Painting
                <div class="arrow">↓</div>

                JavaScript Executes as Needed
                <div class="arrow">↓</div>

                <strong>Webpage Displayed on Screen</strong>
            </div>
        </section>

        <section class="section">
            <h2>4. Important Terms</h2>

            <ul>
                <li><strong>URL:</strong> The address used to locate a web resource.</li>
                <li><strong>DNS:</strong> A system that translates domain names into IP addresses.</li>
                <li><strong>IP Address:</strong> An address used to identify a device or network endpoint.</li>
                <li><strong>HTTP:</strong> A protocol used to transfer web resources.</li>
                <li><strong>HTTPS:</strong> HTTP protected by TLS encryption.</li>
                <li><strong>DOM:</strong> A structured representation of an HTML document.</li>
                <li><strong>CSSOM:</strong> A representation of the CSS rules applied to a document.</li>
                <li><strong>Rendering:</strong> The process of turning document content and styles into visible output.</li>
            </ul>
        </section>

        <section class="section" id="conclusion">
            <h2>5. Conclusion</h2>

            <p>
                When a user enters a URL, the browser performs several
                operations involving caching, DNS, network connections,
                HTTP communication, and page rendering. It retrieves the
                required resources, processes HTML and CSS, executes
                JavaScript when appropriate, and displays the result.
            </p>

            <p>
                Understanding this process helps us learn how websites work
                and provides a foundation for studying web development,
                networking, and browser technology.
            </p>
        </section>

    </main>

    <footer>
        <p>Web Technology Assignment 1</p>
        <p>Topic: What Happens Between Typing a URL and Seeing the Page?</p>
    </footer>

</body>
</html>
