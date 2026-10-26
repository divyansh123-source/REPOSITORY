<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 3 - Terminal Navigation Practice</title>

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
            padding: 42px 20px;
        }

        header h1 {
            font-size: 30px;
            margin-bottom: 10px;
        }

        nav {
            background: #111827;
            text-align: center;
            padding: 14px;
        }

        nav a {
            color: white;
            text-decoration: none;
            margin: 0 12px;
            font-weight: bold;
        }

        nav a:hover {
            color: #93c5fd;
        }

        .container {
            max-width: 1100px;
            width: 94%;
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
            margin: 18px 0 8px;
        }

        p {
            margin-bottom: 12px;
        }

        .table-wrap {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            min-width: 700px;
        }

        th, td {
            padding: 12px;
            border: 1px solid #cbd5e1;
            text-align: left;
        }

        th {
            background: #1d4ed8;
            color: white;
        }

        tr:nth-child(even) {
            background: #f1f5f9;
        }

        code {
            background: #e2e8f0;
            color: #be123c;
            padding: 3px 6px;
            border-radius: 4px;
            font-family: Consolas, monospace;
            white-space: nowrap;
        }

        pre {
            background: #111827;
            color: #a7f3d0;
            padding: 18px;
            border-radius: 8px;
            overflow-x: auto;
            margin: 15px 0;
            font-size: 14px;
            line-height: 1.9;
        }

        .task {
            background: #eff6ff;
            border-left: 5px solid #2563eb;
            padding: 15px;
            margin: 12px 0;
            border-radius: 6px;
        }

        .note {
            background: #fef3c7;
            border-left: 5px solid #f59e0b;
            padding: 15px;
            border-radius: 6px;
            margin-top: 15px;
        }

        .success {
            background: #ecfdf5;
            border-left: 5px solid #059669;
            padding: 15px;
            border-radius: 6px;
            margin-top: 15px;
        }

        ol, ul {
            padding-left: 25px;
        }

        li {
            margin-bottom: 9px;
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

            .section {
                padding: 18px;
            }
        }
    </style>
</head>

<body>

    <header>
        <h1>Assignment 3</h1>
        <p>Terminal Navigation Practice Sheet</p>
        <p>Learning Basic Command-Line Operations</p>
    </header>

    <nav>
        <a href="#introduction">Introduction</a>
        <a href="#commands">Commands</a>
        <a href="#practice">Practice Exercise</a>
        <a href="#answers">Answers</a>
        <a href="#conclusion">Conclusion</a>
    </nav>

    <main class="container">

        <section class="section" id="introduction">
            <h2>1. Introduction</h2>

            <p>
                A terminal is a text-based interface that allows users
                to interact with an operating system by entering commands.
                It is useful for navigating folders, managing files,
                creating directories, and opening development projects.
            </p>

            <p>
                This practice sheet covers common terminal commands
                for macOS, Linux, Git Bash, and Windows PowerShell.
            </p>
        </section>

        <section class="section" id="commands">
            <h2>2. Terminal Commands Reference</h2>

            <p>
                The following table lists common commands and their
                PowerShell equivalents where applicable.
            </p>

            <div class="table-wrap">
                <table>
                    <thead>
                        <tr>
                            <th>#</th>
                            <th>Task</th>
                            <th>macOS / Linux / Git Bash</th>
                            <th>PowerShell</th>
                        </tr>
                    </thead>

                    <tbody>
                        <tr>
                            <td>1</td>
                            <td>Show current folder</td>
                            <td><code>pwd</code></td>
                            <td><code>pwd</code></td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td>List files</td>
                            <td><code>ls</code></td>
                            <td><code>ls</code></td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td>List details and hidden files</td>
                            <td><code>ls -la</code></td>
                            <td><code>ls -Force</code></td>
                        </tr>
                        <tr>
                            <td>4</td>
                            <td>Create a folder</td>
                            <td><code>mkdir practice</code></td>
                            <td><code>mkdir practice</code></td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td>Enter a folder</td>
                            <td><code>cd practice</code></td>
                            <td><code>cd practice</code></td>
                        </tr>
                        <tr>
                            <td>6</td>
                            <td>Create an empty file</td>
                            <td><code>touch index.html</code></td>
                            <td><code>New-Item index.html -ItemType File</code></td>
                        </tr>
                        <tr>
                            <td>7</td>
                            <td>Create nested folders</td>
                            <td><code>mkdir -p css/images</code></td>
                            <td><code>mkdir css/images</code></td>
                        </tr>
                        <tr>
                            <td>8</td>
                            <td>Go up one level</td>
                            <td><code>cd ..</code></td>
                            <td><code>cd ..</code></td>
                        </tr>
                        <tr>
                            <td>9</td>
                            <td>Go to home directory</td>
                            <td><code>cd ~</code></td>
                            <td><code>cd ~</code></td>
                        </tr>
                        <tr>
                            <td>10</td>
                            <td>Copy a file</td>
                            <td><code>cp index.html backup.html</code></td>
                            <td><code>Copy-Item index.html backup.html</code></td>
                        </tr>
                        <tr>
                            <td>11</td>
                            <td>Rename or move a file</td>
                            <td><code>mv backup.html old.html</code></td>
                            <td><code>Rename-Item backup.html old.html</code></td>
                        </tr>
                        <tr>
                            <td>12</td>
                            <td>Delete a file</td>
                            <td><code>rm old.html</code></td>
                            <td><code>Remove-Item old.html</code></td>
                        </tr>
                        <tr>
                            <td>13</td>
                            <td>Delete a folder and its contents</td>
                            <td><code>rm -r css</code></td>
                            <td><code>Remove-Item css -Recurse</code></td>
                        </tr>
                        <tr>
                            <td>14</td>
                            <td>Print file contents</td>
                            <td><code>cat index.html</code></td>
                            <td><code>Get-Content index.html</code></td>
                        </tr>
                        <tr>
                            <td>15</td>
                            <td>Clear the screen</td>
                            <td><code>clear</code></td>
                            <td><code>Clear-Host</code></td>
                        </tr>
                        <tr>
                            <td>16</td>
                            <td>Open folder in VS Code</td>
                            <td><code>code .</code></td>
                            <td><code>code .</code></td>
                        </tr>
                    </tbody>
                </table>
            </div>

            <div class="note">
                <strong>Note:</strong>
                Commands may differ slightly between shells. In PowerShell,
                <code>mkdir css/images</code> can create nested directories
                when the parent directory does not already exist in common
                modern PowerShell versions. If it fails, create each
                directory separately. Use delete commands carefully.
            </div>
        </section>

        <section class="section" id="practice">
            <h2>3. Practice Exercise</h2>

            <p>
                Starting from your home directory, complete the following
                tasks using the terminal.
            </p>

            <div class="task">
                <strong>Task 1:</strong>
                Create a folder named <code>website</code> containing
                <code>index.html</code>, <code>css/style.css</code>,
                and an <code>images</code> folder.
            </div>

            <div class="task">
                <strong>Task 2:</strong>
                Enter the <code>css</code> directory and return to
                <code>website</code> using a single command:
                <code>cd ..</code>.
            </div>

            <div class="task">
                <strong>Task 3:</strong>
                List all files and folders recursively using
                <code>ls -R</code>.
            </div>

            <div class="task">
                <strong>Task 4:</strong>
                Rename <code>index.html</code> to <code>home.html</code>
                and then rename it back to <code>index.html</code>.
            </div>

            <div class="task">
                <strong>Task 5:</strong>
                Open the project folder in Visual Studio Code.
            </div>
        </section>

        <section class="section" id="answers">
            <h2>4. Answers: Commands in Order</h2>

            <h3>For macOS, Linux, or Git Bash</h3>

            <pre>cd ~
mkdir -p website/css website/images
touch website/index.html website/css/style.css
cd website/css
cd ..
ls -R
mv index.html home.html
mv home.html index.html
code .</pre>

            <h3>For Windows PowerShell</h3>

            <pre>cd ~
New-Item -ItemType Directory -Force website/css
New-Item -ItemType Directory -Force website/images
New-Item -ItemType File -Force website/index.html
New-Item -ItemType File -Force website/css/style.css
cd website/css
cd ..
Get-ChildItem -Recurse
Rename-Item index.html home.html
Rename-Item home.html index.html
code .</pre>

            <div class="success">
                <strong>Expected folder structure:</strong>
                <pre>website/
├── index.html
├── css/
│   └── style.css
└── images/</pre>
            </div>

            <div class="note">
                <strong>Important:</strong>
                After running <code>cd ..</code> in the exercise,
                the terminal should be inside the <code>website</code>
                folder. The rename commands work from there.
                Run the commands in the order shown and ensure the
                original files exist before renaming them.
            </div>
        </section>

        <section class="section">
            <h2>5. Learning Outcomes</h2>

            <ul>
                <li>Understand how to navigate between directories.</li>
                <li>Learn to list files and inspect directory contents.</li>
                <li>Create folders and files using terminal commands.</li>
                <li>Copy, rename, move, and delete files.</li>
                <li>Open a project folder using Visual Studio Code.</li>
                <li>Understand differences between common terminal shells.</li>
            </ul>
        </section>

        <section class="section" id="conclusion">
            <h2>6. Conclusion</h2>

            <p>
                Terminal commands make file and folder management faster
                and more efficient. Practising these commands helps
                developers navigate projects, organize files, and work
                comfortably with tools such as Visual Studio Code.
            </p>

            <p>
                This assignment provides a foundation for using the
                command line in web development and other programming
                activities.
            </p>
        </section>

    </main>

    <footer>
        <p>Web Development Assignment 3</p>
        <p>Terminal Navigation Practice Sheet</p>
    </footer>

</body>
</html>
