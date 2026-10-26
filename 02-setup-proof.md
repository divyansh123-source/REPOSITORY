<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 2 - Setup Proof</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background: #f1f5f9;
            color: #263445;
            line-height: 1.7;
        }

        header {
            background: linear-gradient(135deg, #172554, #2563eb);
            color: white;
            text-align: center;
            padding: 40px 20px;
        }

        header h1 {
            font-size: 30px;
            margin-bottom: 10px;
        }

        nav {
            background: #111827;
            padding: 14px;
            text-align: center;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 14px;
            font-weight: bold;
        }

        nav a:hover {
            color: #93c5fd;
        }

        .container {
            max-width: 1000px;
            width: 92%;
            margin: 30px auto;
        }

        .section {
            background: white;
            padding: 25px;
            margin-bottom: 25px;
            border-radius: 12px;
            box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
        }

        h2 {
            color: #1d4ed8;
            margin-bottom: 15px;
            border-bottom: 2px solid #dbeafe;
            padding-bottom: 8px;
        }

        h3 {
            color: #1e40af;
            margin: 12px 0 8px;
        }

        .tool-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 18px;
        }

        .tool-card {
            background: #eff6ff;
            border-left: 5px solid #2563eb;
            padding: 18px;
            border-radius: 8px;
        }

        .step {
            margin-bottom: 18px;
            padding: 15px;
            background: #f8fafc;
            border-radius: 8px;
        }

        .number {
            display: inline-block;
            background: #2563eb;
            color: white;
            border-radius: 50%;
            width: 30px;
            height: 30px;
            text-align: center;
            line-height: 30px;
            margin-right: 7px;
            font-weight: bold;
        }

        code {
            background: #e2e8f0;
            color: #be123c;
            padding: 3px 7px;
            border-radius: 4px;
            font-family: Consolas, monospace;
        }

        pre {
            background: #111827;
            color: #a7f3d0;
            padding: 16px;
            border-radius: 8px;
            overflow-x: auto;
            margin: 12px 0;
        }

        .screenshot {
            text-align: center;
            margin-top: 15px;
        }

        .screenshot img {
            width: 100%;
            height: auto;
            border: 2px solid #cbd5e1;
            border-radius: 8px;
        }

        .note {
            background: #fef3c7;
            border-left: 5px solid #f59e0b;
            padding: 15px;
            margin-top: 15px;
            border-radius: 5px;
        }

        .table-wrap {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
        }

        th, td {
            border: 1px solid #cbd5e1;
            padding: 12px;
            text-align: left;
        }

        th {
            background: #1d4ed8;
            color: white;
        }

        tr:nth-child(even) {
            background: #f1f5f9;
        }

        footer {
            background: #172554;
            color: white;
            text-align: center;
            padding: 22px;
            margin-top: 40px;
        }

        @media (max-width: 600px) {
            header h1 {
                font-size: 24px;
            }

            nav a {
                display: inline-block;
                margin: 5px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>Assignment 2: Setup Proof</h1>
        <p>VS Code, Node.js and Live Server</p>
        <p>Web Development Environment Setup</p>
    </header>

    <nav>
        <a href="#introduction">Introduction</a>
        <a href="#tools">Tools</a>
        <a href="#steps">Setup Steps</a>
        <a href="#proof">Screenshot Proof</a>
        <a href="#summary">Summary</a>
    </nav>

    <main class="container">

        <section class="section" id="introduction">
            <h2>1. Introduction</h2>
            <p>
                The purpose of this assignment is to set up and verify
                the basic environment required for web development.
                Visual Studio Code is used to write and edit code,
                Node.js provides a JavaScript runtime, and Live Server
                allows HTML pages to be viewed in a browser with automatic
                reloading during development.
            </p>
        </section>

        <section class="section" id="tools">
            <h2>2. Tools Required</h2>

            <div class="tool-grid">
                <div class="tool-card">
                    <h3>Visual Studio Code</h3>
                    <p>
                        A source-code editor used to create, edit,
                        and manage web development projects.
                    </p>
                </div>

                <div class="tool-card">
                    <h3>Node.js</h3>
                    <p>
                        A JavaScript runtime that allows JavaScript
                        programs to run outside a web browser.
                    </p>
                </div>

                <div class="tool-card">
                    <h3>Live Server</h3>
                    <p>
                        A VS Code extension that serves local web files
                        and refreshes the browser when files change.
                    </p>
                </div>
            </div>
        </section>

        <section class="section" id="steps">
            <h2>3. Installation and Verification Steps</h2>

            <div class="step">
                <h3>
                    <span class="number">1</span>
                    Verify Visual Studio Code
                </h3>
                <p>
                    Open VS Code and select
                    <strong>Help → About</strong> to view the installed
                    version of Visual Studio Code.
                </p>
            </div>

            <div class="step">
                <h3>
                    <span class="number">2</span>
                    Verify Node.js and npm
                </h3>
                <p>
                    Open the integrated terminal in VS Code by pressing
                    <code>Ctrl + `</code>. Run these commands separately:
                </p>

                <pre>node -v
npm -v</pre>

                <p>
                    The commands display the installed Node.js and npm
                    versions. If a command is not recognized, check
                    whether the software is installed and available
                    in your system PATH.
                </p>
            </div>

            <div class="step">
                <h3>
                    <span class="number">3</span>
                    Install Live Server
                </h3>
                <p>
                    Open the Extensions panel using
                    <code>Ctrl + Shift + X</code>. Search for
                    <strong>Live Server by Ritwick Dey</strong>
                    and install the extension.
                </p>
            </div>

            <div class="step">
                <h3>
                    <span class="number">4</span>
                    Run an HTML File
                </h3>
                <p>
                    Open an HTML file in VS Code. Right-click inside
                    the editor and choose
                    <strong>Open with Live Server</strong>, or click
                    <strong>Go Live</strong> in the status bar.
                </p>

                <p>
                    The browser should open the local webpage,
                    commonly at an address such as
                    <code>http://127.0.0.1:5500/</code>.
                    The exact port may differ on your computer.
                </p>
            </div>
        </section>

        <section class="section" id="proof">
            <h2>4. Setup Proof Screenshot</h2>

            <p>
                The screenshot below is intended to document the
                development environment. Capture your own screen with
                VS Code, the terminal output, the Live Server extension,
                and the browser displaying your local webpage.
            </p>

            <div class="screenshot">
                <img
                    src="screenshots/setup-proof.png"
                    alt="Setup proof screenshot showing VS Code, Node.js, Live Server and a local browser page"
                    onerror="this.style.display='none';
                    document.getElementById('missing-image').style.display='block';"
                >

                <div id="missing-image" style="display:none;
                    padding:25px; background:#f1f5f9;
                    border:2px dashed #94a3b8; border-radius:8px;">
                    <h3>Screenshot not added yet</h3>
                    <p>
                        Save your real setup screenshot as
                        <code>screenshots/setup-proof.png</code>
                        inside this project folder.
                    </p>
                </div>
            </div>

            <div class="note">
                <strong>Important:</strong>
                The screenshot must come from your actual computer.
                Do not use a sample image as proof of installation.
            </div>
        </section>

        <section class="section">
            <h2>5. Software Version and Verification Table</h2>

            <p>
                Fill in the actual versions displayed on your computer
                before submitting the assignment.
            </p>

            <div class="table-wrap">
                <table>
                    <thead>
                        <tr>
                            <th>Tool</th>
                            <th>Version</th>
                            <th>Installation Status</th>
                        </tr>
                    </thead>

                    <tbody>
                        <tr>
                            <td>Visual Studio Code</td>
                            <td>Enter your installed version</td>
                            <td>Verify on your computer</td>
                        </tr>

                        <tr>
                            <td>Node.js</td>
                            <td>Enter the output of node -v</td>
                            <td>Verify on your computer</td>
                        </tr>

                        <tr>
                            <td>npm</td>
                            <td>Enter the output of npm -v</td>
                            <td>Verify on your computer</td>
                        </tr>

                        <tr>
                            <td>Live Server</td>
                            <td>Enter the installed extension version</td>
                            <td>Verify on your computer</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section class="section" id="summary">
            <h2>6. Conclusion</h2>
            <p>
                In this assignment, the setup and verification process
                for Visual Studio Code, Node.js, npm, and Live Server
                has been documented. These tools provide a basic
                environment for creating and testing HTML, CSS,
                and JavaScript projects.
            </p>

            <p>
                The final screenshot and software version details
                provide evidence of the setup performed on the
                student's computer.
            </p>
        </section>

    </main>

    <footer>
        <p>Web Development Assignment 2</p>
        <p>Setup Proof: VS Code, Node.js and Live Server</p>
    </footer>

</body>
</html>
