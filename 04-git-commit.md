<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Assignment 4 - Git Repository and Commits</title>

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
            max-width: 1050px;
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
            margin: 18px 0 8px;
        }

        p {
            margin-bottom: 12px;
        }

        ul, ol {
            padding-left: 25px;
        }

        li {
            margin-bottom: 8px;
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

        code {
            background: #e2e8f0;
            color: #be123c;
            padding: 3px 6px;
            border-radius: 4px;
            font-family: Consolas, monospace;
        }

        .note {
            background: #fef3c7;
            border-left: 5px solid #f59e0b;
            padding: 15px;
            margin-top: 15px;
            border-radius: 6px;
        }

        .info-card {
            background: #eff6ff;
            border-left: 5px solid #2563eb;
            padding: 16px;
            margin: 12px 0;
            border-radius: 6px;
        }

        .table-wrap {
            overflow-x: auto;
        }

        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            min-width: 550px;
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

        .success {
            background: #ecfdf5;
            border-left: 5px solid #059669;
            padding: 15px;
            border-radius: 6px;
            margin-top: 15px;
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
        <h1>Assignment 4</h1>
        <p>Git Repository with at Least Three Meaningful Commits</p>
        <p>Version Control and Project Management</p>
    </header>

    <nav>
        <a href="#introduction">Introduction</a>
        <a href="#setup">Git Setup</a>
        <a href="#commits">Three Commits</a>
        <a href="#messages">Commit Rules</a>
        <a href="#history">History</a>
        <a href="#conclusion">Conclusion</a>
    </nav>

    <main class="container">

        <section class="section" id="introduction">
            <h2>1. Introduction</h2>

            <p>
                Git is a distributed version control system used to track
                changes in files and collaborate on software projects.
                A repository stores project files and their version history.
            </p>

            <p>
                The objective of this assignment is to create a Git
                repository, configure the user's identity, organize
                project files, and record at least three meaningful commits.
            </p>
        </section>

        <section class="section" id="setup">
            <h2>2. Configure Git Identity</h2>

            <p>
                Before creating commits, configure your name and email
                address. Replace the example values with your own details.
            </p>

            <pre>git config --global user.name "Your Name"
git config --global user.email "you@example.com"</pre>

            <p>
                These settings identify the author of your commits.
                The global option applies the settings to your user
                account unless a repository has its own configuration.
            </p>
        </section>

        <section class="section">
            <h2>3. Create the Repository</h2>

            <p>
                Open the terminal in VS Code and run the following
                commands to create a repository named
                <code>html-css-assignments</code>.
            </p>

            <pre>mkdir html-css-assignments
cd html-css-assignments
git init
git branch -M main</pre>

            <div class="info-card">
                <strong>Explanation:</strong>
                <ul>
                    <li><code>mkdir</code> creates the project directory.</li>
                    <li><code>cd</code> enters the directory.</li>
                    <li><code>git init</code> initializes a Git repository.</li>
                    <li><code>git branch -M main</code> names the current branch main.</li>
                </ul>
            </div>
        </section>

        <section class="section" id="commits">
            <h2>4. Create Three Meaningful Commits</h2>

            <h3>Commit 1: Add the README file</h3>

            <p>
                Create a README file to describe the purpose of the project.
            </p>

            <pre>echo "# HTML &amp; CSS Assignments" > README.md
git add README.md
git commit -m "docs: add README with project overview"</pre>

            <h3>Commit 2: Add Assignments 1–5</h3>

            <p>
                Copy your assignment files into the repository, then
                stage and commit the files that belong to this change.
            </p>

            <pre>git add 01-*.md 02-*.md 03-*.md 04-*.md 05-*.md
git commit -m "docs: add setup &amp; git assignments (1-5)"</pre>

            <h3>Commit 3: Add HTML Basics Assignments</h3>

            <p>
                Stage and commit the HTML assignment files for assignments
                6–10, assuming these files exist in your repository.
            </p>

            <pre>git add 06-*.html 07-*.html 08-*.html 09-*.html 10-*.html
git commit -m "feat: add HTML basics assignments (6-10)"</pre>

            <div class="note">
                <strong>Important:</strong>
                These commands assume your files use the specified
                numbered filenames. Adjust the filenames or paths to
                match your actual project. Git cannot commit files
                that do not exist or have not been staged.
            </div>
        </section>

        <section class="section" id="messages">
            <h2>5. Good Commit-Message Rules</h2>

            <div class="info-card">
                <h3>Use imperative wording</h3>
                <p>
                    Describe the change as an action, such as
                    <code>add navbar</code>, rather than
                    <code>added navbar</code>.
                </p>
            </div>

            <div class="info-card">
                <h3>Use a type prefix</h3>
                <p>
                    Prefixes make it easier to understand the purpose
                    of a commit.
                </p>
                <ul>
                    <li><code>feat:</code> Adds a feature.</li>
                    <li><code>fix:</code> Fixes a problem.</li>
                    <li><code>docs:</code> Changes documentation.</li>
                    <li><code>style:</code> Changes formatting or styling.</li>
                    <li><code>refactor:</code> Restructures code without changing its intended behavior.</li>
                </ul>
            </div>

            <div class="info-card">
                <h3>Keep commits focused</h3>
                <p>
                    Each commit should represent one logical change,
                    making the project history easier to review and maintain.
                </p>
            </div>
        </section>

        <section class="section" id="history">
            <h2>6. Suggested Commit History for the Course</h2>

            <div class="table-wrap">
                <table>
                    <thead>
                        <tr>
                            <th>Commit</th>
                            <th>Commit Message</th>
                            <th>Purpose</th>
                        </tr>
                    </thead>

                    <tbody>
                        <tr>
                            <td>1</td>
                            <td><code>docs: add README</code></td>
                            <td>Document the project.</td>
                        </tr>
                        <tr>
                            <td>2</td>
                            <td><code>docs: setup &amp; git assignments (1-5)</code></td>
                            <td>Add initial setup and Git work.</td>
                        </tr>
                        <tr>
                            <td>3</td>
                            <td><code>feat: HTML basics (6-10)</code></td>
                            <td>Add basic HTML assignments.</td>
                        </tr>
                        <tr>
                            <td>4</td>
                            <td><code>feat: links, images, lists (11-15)</code></td>
                            <td>Practice HTML links, images, and lists.</td>
                        </tr>
                        <tr>
                            <td>5</td>
                            <td><code>feat: forms, tables, metadata (16-20)</code></td>
                            <td>Practice forms and tables.</td>
                        </tr>
                        <tr>
                            <td>6</td>
                            <td><code>style: CSS fundamentals (21-25)</code></td>
                            <td>Introduce basic CSS.</td>
                        </tr>
                        <tr>
                            <td>7</td>
                            <td><code>style: box model &amp; positioning (26-30)</code></td>
                            <td>Practice layout and positioning.</td>
                        </tr>
                        <tr>
                            <td>8</td>
                            <td><code>feat: flexbox layouts (31-35)</code></td>
                            <td>Create flexible page layouts.</td>
                        </tr>
                        <tr>
                            <td>9</td>
                            <td><code>feat: grid layouts (36-40)</code></td>
                            <td>Build CSS Grid layouts.</td>
                        </tr>
                        <tr>
                            <td>10</td>
                            <td><code>feat: responsive landing page (41-45)</code></td>
                            <td>Create a responsive landing page.</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </section>

        <section class="section">
            <h2>7. Verify the Repository History</h2>

            <p>
                After making the commits, run this command to view
                the repository's commit history.
            </p>

            <pre>git log --oneline</pre>

            <p>
                The terminal displays a short commit hash and commit
                message for each commit. Confirm that at least three
                commits appear in the history.
            </p>

            <div class="success">
                <strong>Expected result:</strong>
                Your repository should contain a README file,
                your assignment files, and at least three separate,
                meaningful commits.
            </div>
        </section>

        <section class="section" id="conclusion">
            <h2>8. Conclusion</h2>

            <p>
                This assignment demonstrates how Git can be used to
                initialize a repository, configure author information,
                track project files, and maintain a useful history
                through meaningful commits.
            </p>

            <p>
                Using clear commit messages and making focused changes
                helps developers maintain organized projects and
                collaborate more effectively.
            </p>
        </section>

    </main>

    <footer>
        <p>Web Development Assignment 4</p>
        <p>Git Repository and Version Control</p>
    </footer>

</body>
</html>
