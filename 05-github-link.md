<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Assignment 5 - GitHub Repository</title>

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
            background: linear-gradient(135deg, #171717, #374151);
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
            padding: 14px;
            text-align: center;
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
            width: 92%;
            max-width: 1000px;
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
            color: #2563eb;
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

        ol, ul {
            padding-left: 25px;
        }

        li {
            margin-bottom: 10px;
        }

        code {
            background: #e2e8f0;
            color: #be123c;
            padding: 3px 6px;
            border-radius: 4px;
            font-family: Consolas, monospace;
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

        .step {
            background: #eff6ff;
            border-left: 5px solid #2563eb;
            padding: 16px;
            margin: 14px 0;
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
            padding: 18px;
            border-radius: 6px;
        }

        .repo-card {
            background: #f8fafc;
            border: 1px solid #cbd5e1;
            padding: 20px;
            border-radius: 10px;
            overflow-wrap: anywhere;
        }

        .repo-link {
            color: #2563eb;
            font-weight: bold;
            text-decoration: none;
        }

        .repo-link:hover {
            text-decoration: underline;
        }

        footer {
            background: #171717;
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
        <h1>Assignment 5</h1>
        <p>GitHub Repository Link</p>
        <p>Uploading and Hosting a Web Development Project</p>
    </header>

    <nav>
        <a href="#introduction">Introduction</a>
        <a href="#create">Create Repository</a>
        <a href="#push">Push Code</a>
        <a href="#pages">GitHub Pages</a>
        <a href="#submission">Submission</a>
    </nav>

    <main class="container">

        <section class="section" id="introduction">
            <h2>1. Introduction</h2>

            <p>
                GitHub is an online platform used to store, manage,
                and share projects using Git version control.
                Developers can upload their source code, maintain
                commit history, collaborate with others, and publish
                static websites.
            </p>

            <p>
                The objective of this assignment is to create a GitHub
                repository, push the local HTML and CSS project to it,
                verify the uploaded files, and optionally host the
                project using GitHub Pages.
            </p>
        </section>

        <section class="section" id="create">
            <h2>2. Create a GitHub Repository</h2>

            <div class="step">
                <h3>Step 1: Open GitHub</h3>
                <p>
                    Visit the official GitHub website and sign in
                    to your account.
                </p>
                <p>
                    Website:
                    <a class="repo-link"
                       href="https://github.com/"
                       target="_blank"
                       rel="noopener noreferrer">
                        https://github.com/
                    </a>
                </p>
            </div>

            <div class="step">
                <h3>Step 2: Create a New Repository</h3>
                <ol>
                    <li>Click the New repository option.</li>
                    <li>Enter <code>html-css-assignments</code> as the repository name.</li>
                    <li>Choose Public or Private according to your requirements.</li>
                    <li>Leave the repository initialization options unchecked if your local project already has a README.</li>
                    <li>Click Create repository.</li>
                </ol>
            </div>
        </section>

        <section class="section" id="push">
            <h2>3. Push the Local Project to GitHub</h2>

            <p>
                Open the terminal in VS Code and move into your
                existing local repository folder.
            </p>

            <h3>Step 1: Add the Remote Repository</h3>

            <p>
                Replace <code>YOUR-USERNAME</code> with your actual
                GitHub username.
            </p>

            <pre>git remote add origin https://github.com/YOUR-USERNAME/html-css-assignments.git</pre>

            <h3>Step 2: Set the Main Branch</h3>

            <pre>git branch -M main</pre>

            <h3>Step 3: Push the Commits</h3>

            <pre>git push -u origin main</pre>

            <div class="note">
                <strong>Note:</strong>
                If the remote named origin already exists, do not
                repeat the first command. Check it using
                <code>git remote -v</code>. If necessary, update it
                using <code>git remote set-url origin YOUR-REPOSITORY-URL</code>.
            </div>

            <h3>Step 4: Verify the Upload</h3>

            <p>
                Refresh the repository page on GitHub. Check that
                your files, README, and commit history are visible.
            </p>

            <div class="success">
                <strong>Expected result:</strong>
                Your local project should be available in your GitHub
                repository, with the commits you created in Assignment 4.
            </div>
        </section>

        <section class="section" id="pages">
            <h2>4. Optional: Host the Website Using GitHub Pages</h2>

            <p>
                GitHub Pages can publish a static website directly
                from a repository.
            </p>

            <ol>
                <li>Open your repository on GitHub.</li>
                <li>Go to Settings.</li>
                <li>Select Pages from the sidebar.</li>
                <li>Under Build and deployment, select Deploy from a branch.</li>
                <li>Choose the <code>main</code> branch and the <code>/(root)</code> folder.</li>
                <li>Click Save.</li>
                <li>Wait for GitHub Pages to finish deploying the site.</li>
            </ol>

            <h3>Website URL Format</h3>

            <pre>https://YOUR-USERNAME.github.io/html-css-assignments/</pre>

            <p>
                Replace <code>YOUR-USERNAME</code> with your GitHub
                username. The website will be available after a
                successful deployment, provided the repository
                and Pages settings permit publication.
            </p>
        </section>

        <section class="section" id="submission">
            <h2>5. Assignment Submission</h2>

            <p>
                Enter your actual GitHub repository URL below
                after uploading the project.
            </p>

            <div class="repo-card">
                <h3>Repository Link</h3>
                <p>
                    <a class="repo-link"
                       href="https://github.com/"
                       target="_blank"
                       rel="noopener noreferrer">
                        Open GitHub
                    </a>
                </p>

                <p>
                    Repository URL format:
                </p>

                <code>https://github.com/YOUR-USERNAME/html-css-assignments</code>
            </div>

            <div class="note">
                <strong>Before submitting:</strong>
                Replace the example username with your real username
                and confirm that the repository link opens correctly.
                Do not submit the placeholder URL as your final link.
            </div>
        </section>

        <section class="section">
            <h2>6. Learning Outcomes</h2>

            <ul>
                <li>Understand the purpose of GitHub repositories.</li>
                <li>Connect a local Git repository to a remote repository.</li>
                <li>Upload project files and commits using Git.</li>
                <li>Verify repository contents and commit history.</li>
                <li>Learn the basics of publishing static websites with GitHub Pages.</li>
            </ul>
        </section>

        <section class="section">
            <h2>7. Conclusion</h2>

            <p>
                This assignment demonstrates how a local web development
                project can be uploaded to GitHub using Git commands.
                A remote repository provides an online copy of the
                project and preserves its version history.
            </p>

            <p>
                GitHub Pages can also be used to publish a static
                website, making the project accessible through a
                web browser.
            </p>
        </section>

    </main>

    <footer>
        <p>Web Development Assignment 5</p>
        <p>GitHub Repository and Project Hosting</p>
    </footer>

</body>
</html>
