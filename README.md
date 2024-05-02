# Devops Projects

Welcome to the DevOps Projects repository! This collection of projects is designed to provide hands-on experience and practical learning opportunities in the field of DevOps. Each project is carefully crafted to introduce essential concepts, tools, and practices that are integral to the DevOps methodology. Whether you're a beginner looking to dive into DevOps or an experienced practitioner seeking to sharpen your skills, these projects offer a structured pathway for continuous growth and development.

Feel free to explore the projects below and embark on your DevOps journey!

---

## Project 1: Setting Up Development Environment with GitHub and VSCode

Project 1 serves as an introductory project focusing on setting up a development environment using GitHub for version control and VSCode as the integrated development environment (IDE). This project aims to familiarize the trainee with essential tools and practices commonly used in software development.

**Project 1: Setting Up Development Environment with GitHub and VSCode**

- **Difficulty Level:** Beginner
- **Quick Description:** Create a GitHub account, initialize a repository for project notes, set up VSCode with essential extensions, and perform basic Git operations.
- **Technologies Involved:** GitHub, VSCode, Git.
- **Prerequisites:** None.
- **Steps:**

  1. Create a GitHub account if you haven't already.
  2. Create a new repository to store project notes (e.g., `devops-project-notes`).
  3. Use the GitHub web interface to create a simple `README.md` file using Markdown.
  4. Choose a directory for storing future project files (e.g., `C:\dojo\devops\projects`)
  5. Install VSCode on your local machine.
  6. Log in to GitHub via VSCode and sync configurations.
  7. Install essential VSCode extensions: 
     - Bash extension pack
     - Code Spell Checker
     - Greek - Code Spell Checker
     - GitHub Theme
     - JSON
     - YAML
     - XML
     - Markdown All in One
     - Markdown Preview Enhanced
     - Markdown Table
     - Markdownlint
     - Rainbow CSV
     - Remote - SSH
  8. Set the VSCode theme to GitHub Dark.
  9. Open the `C:\dojo\devops\projects` folder in VSCode.
  10. Install Git on your local machine from git-scm.com.
  11. In the VSCode terminal, clone the repository created in step 2 (`git clone <repository_url>`).
  12. Provide your GitHub credentials in the terminal if the repository is private.
  13. Create a folder named `project1` within the `C:\dojo\devops\projects`.
  14. Add some files to the `project1` folder.
  15. Use Git commands (`git add`, `git commit`, `git push`) to stage and push changes to the remote repository.
  16. Confirm changes on GitHub and check out the Source Control view in VSCode.

- **Documentation Tasks:** 
  - Guide for creating a GitHub account and initializing a repository.
  - Instructions for installing VSCode and essential extensions.
  - Step-by-step guide for performing basic Git operations.
- **Diagrams:**
  - None.
- **Delivery Report:**
  - Summary of the development environment setup, including screenshots of VSCode and GitHub.
  - Troubleshooting guide for common setup issues.

---

## Project 2: Building a Linux VM Lab

This project is a great starting point for someone who wants to learn DevOps. It provides a structured approach to getting hands-on experience with essential concepts like virtualization, networking, Linux operating systems, and SSH connections.

The step-by-step instructions make it accessible for beginners, while also introducing them to important DevOps tools and practices. By completing this project, the trainee will gain practical experience in setting up virtual environments, which is foundational knowledge for DevOps.

Additionally, the project encourages self-learning by introducing concepts like networking and SSH as "black box" components, allowing the trainee to explore and deepen their understanding at their own pace. This approach promotes a growth mindset and empowers the trainee to take ownership of their learning journey.

As the trainee progresses through more advanced projects, they can build upon the knowledge and skills gained from this first project, gradually expanding their understanding of DevOps principles and practices. Overall, this project sets a solid foundation for learning DevOps and provides a pathway for continuous growth and development in the field.

**Project 2: Building a Linux VM Lab**

- **Difficulty Level:** Easy
- **Quick Description:** Create Oracle Linux 9 virtual machines in VirtualBox, configure networking, and set up SSH connections between them.
- **Technologies Involved:** VirtualBox, Oracle Linux, SSH.
- **Prerequisites:** Basic understanding of virtualization and networking concepts.
- **Steps:**

  1. Set up VirtualBox on your local machine.
  2. Create a new NAT Network and a Host Only Network in VirtualBox.
  3. Create VM1 with Oracle Linux 9 and GUI, connecting it to the newly created networks.
  4. Use Putty to SSH to VM1 from the host machine.
  5. Install Asbru Connection Manager on VM1 for managing SSH connections.
  6. Create VM2 with Oracle Linux 9 minimal installation on the same NAT Network.
  7. SSH from VM1 to VM2 using Asbru Connection Manager.

- **Doumentation Tasks:**
  - Installation guides for VirtualBox, Oracle Linux 9, and Asbru Connection Manager.
  - Configuration steps for setting up networking and SSH connections.
  - Troubleshooting tips for common issues. Include draw.io in (Diagrams:).
- **Diagrams:**
  - Network topology showing the NAT Network and Host Only Network.
  - Diagram illustrating the SSH connection between VM1 and VM2. (draw.io)
- **Delivery Report:**
  - Summary of the VM setup, networking configuration, and SSH connection establishment, including screenshots. 
  - Troubleshooting guide for common setup issues.

---

## Project 3: Nginx Web Server and Git Deployment

Project 3 focuses on enhancing the Linux virtual machines (**VM1** and **VM2**) created in Project 2 by installing Nginx web server on **VM2** and deploying a basic HelloWorld HTML page from GitHub using Git. This project also covers snapshotting VMs for restoration, troubleshooting common issues, and exploring Nginx logs.

**Project 3: Nginx Web Server and Git Deployment**

- **Difficulty Level:** Intermediate
- **Quick Description:** Snapshot **VM1** and **VM2** for easy restoration, install Nginx and Git on **VM2**, deploy a basic HelloWorld HTML page served by Nginx.
- **Technologies Involved:** VirtualBox, Oracle Linux, Nginx, Git.
- **Prerequisites:** Completion of Project 2.
- **Steps:**

  1. Take snapshots of both **VM1** and **VM2** for easy restoration in case of issues.
  2. Install Nginx on **VM2** using package manager (`sudo dnf install nginx`).
  3. Install Git on **VM2** (`sudo dnf install git`).
  4. Clone a basic HelloWorld HTML repository from GitHub onto **VM2**:
     - Repository URL: <https://github.com/ithinkihaveacat/hello-world-html.git>
     - Command to clone: `git clone https://github.com/ithinkihaveacat/hello-world-html.git /usr/share/nginx/html`
  5. Configure Nginx to serve the HelloWorld HTML page from the specified directory (`/usr/share/nginx/html`).
  6. Enable Nginx using systemctl (`sudo systemctl enable nginx`) and start the service (`sudo systemctl start nginx`).
  7. Check the status of Nginx service using systemctl (`sudo systemctl status nginx`).
  8. Test the HelloWorld webpage functionality by accessing it locally on **VM2** using `curl localhost`.
  9. Test the HelloWorld webpage accessibility from **VM1** to **VM2** using `curl <VM2_IP>`.
  10. Allow **_HTTP_** (port **_80_**) traffic on **VM2**'s firewall using `firewall-cmd`.
  11. Research and understand the basics of **_HTTP_**, **_HTTPS_**, port **_80_**, and port **_443_**.
  12. Test the HelloWorld webpage accessibility from **VM1** using a browser like Firefox.
  13. Set up port forwarding in VirtualBox Network Manager to forward port **_80_** from **VM2** to port **_50080_** on the host machine.
  14. Access the HelloWorld webpage from the host machine's browser using **_localhost:50080_**.
  15. Locate and explore other Nginx logs such as error logs (`/var/log/nginx/error.log`).
  16. Monitor Nginx logs using `tail -100f /var/log/nginx/access.log` to observe live access logs while accessing the webpage.

- **Documentation Tasks:**
  - Guide for taking snapshots of VMs and restoring them.
  - Installation instructions for Nginx and Git on **VM2**.
  - Deployment guide for pulling the HelloWorld repository and configuring Nginx.
  - Troubleshooting tips for common setup issues related to Nginx configuration and firewall settings.
- **Diagrams:**
  - None.
- **Delivery Report:**
  - Summary of the enhancements made to VMs, including screenshots of Nginx configuration and successful webpage access.
  - Troubleshooting guide for common setup issues related to Nginx and Git deployment.

---

Certainly! Here's a consolidated recap of the above projects merged together:

---

## Recap untilnow

- **Difficulty Levels:**
  - Project 1: Beginner
  - Project 2: Easy
  - Project 3: Intermediate

- **Technologies Involved:**
  - Virtualization: VirtualBox
  - Operating System: Oracle Linux 9
  - Version Control: GitHub, Git
  - Integrated Development Environment: VSCode
  - Web Server: Nginx
  - Other Tools: Asbru Connection Manager, curl, firewall-cmd

- **Outline of VMs and Services Running:**
  - **VM1:**
    - Oracle Linux 9 with GUI
    - SSH service running
  - **VM2:**
    - Oracle Linux 9 minimal installation
    - Nginx web server running
    - SSH service running

- **Outline of Local Machine Apps Installed and Explored:**
  - VSCode with essential extensions
  - Git
  - Nginx
  - Firefox (or any available browser)
  - Putty (for SSH connection to VM1)

- **Network Protocols Engaged:**
  - HTTP
  - SSH

- **Commands Used in Linux:**
  - Package installation: `sudo dnf install <package>`
  - Git operations: `git clone`, `git add`, `git commit`, `git push`
  - Nginx service management: `sudo systemctl enable/start/status nginx`
  - Firewall configuration: `firewall-cmd`

- **Diagrams Created:**
  - Network topology diagram showing NAT Network and Host Only Network
  - Diagram illustrating the SSH connection between VM1 and VM2

This series of projects provided hands-on experience in setting up virtual environments, configuring networking, deploying web services, and utilizing essential DevOps tools. Through practical tasks and exploration, trainees gained foundational knowledge in DevOps principles and practices.

---

Here's the updated project outline:

---

## Project 4: Setting Up a Simple CI/CD Pipeline with Jenkins

This project focuses on setting up a basic Continuous Integration/Continuous Deployment (CI/CD) pipeline using Jenkins. You'll automate the deployment of a HelloWorld project to a virtual machine (**VM2**) running Nginx, triggered by changes pushed to a private GitHub repository.

**Project 4: Setting Up a Simple CI/CD Pipeline with Jenkins**

- **Difficulty Level:** Intermediate
- **Technologies Involved:** Jenkins, Git, GitHub, VirtualBox, Oracle Linux
- **Prerequisites:** Completion of Project 3

**Steps:**

1. **Download HelloWorld Project:**
   - Clone the HelloWorld project from a public GitHub repository into a folder named `hello-world-html-new`:
     ```
     git clone https://github.com/ithinkihaveacat/hello-world-html.git hello-world-html-new
     ```

2. **Create New Repository on GitHub:**
   - Go to your GitHub account in a web browser and create a new repository named `hello-world-html-new`. Make sure to leave it empty without initializing it with a README, since you'll be pushing an existing repository into it.

3. **Change Remote URL:**
   - Change the remote URL to point to the new GitHub repository:
     ```
     git remote set-url origin <new_repo_url>
     ```
   - Replace `<new_repo_url>` with the URL of the new repository you created on GitHub.

4. **Upload Project to GitHub:**
   - Initialize a new Git repository locally:
     ```
     git init
     ```
   - Add the HelloWorld project:
     ```
     git add .
     ```
   - Commit changes:
     ```
     git commit -m "Initial commit"
     ```
   - Push to the private GitHub repository:
     ```
     git push -u origin master
     ```

5. **Make Changes to Index.html:**
   - Open index.html file in a text editor.
   - Modify the content to display `Hello, World! NEW` instead of `Hello, World!`.

6. **Push Changes to GitHub Repo:**
   - Add and commit the changes:
     ```
     git add index.html
     git commit -m "Update greeting message"
     ```
   - Push changes to the private GitHub repository:
     ```
     git push
     ```

7. **Create VM3:**
   - Create a new VM (**VM3**) with Oracle Linux 9 minimal installation, adding it to the same NAT network as **VM1** and **VM2**, and also adding a Host Only network.

8. **Install Jenkins on VM3:**
   - Install Jenkins on **VM3** using the package manager:
     ```
     sudo dnf install jenkins
     ```

9. **Configure Firewall and SELinux:**
   - If needed, fix firewall rules and disable SELinux on **VM3** to ensure Jenkins functions properly.

10. **Set Up Jenkins Job:**
    - Access Jenkins from **VM1** using VM3 IP or port forward port 8080 of **VM3** to 50081 on the local machine.
    - Create a new Jenkins job, specifying the Git repository URL and credentials to access it.

11. **Deploy to VM2 Using SSH:**
    - Set up Jenkins to deploy the project to **VM2** using SSH to the proper Nginx directory.

12. **Confirm Deployment:**
    - Test the deployment from **VM2** using:
      ```
      curl localhost
      ```
    - Test the deployment from **VM1** using:
      ```
      curl <VM2_IP>
      ```
    - Test the deployment from **VM1** using a browser.

13. **Make Changes and Push Again:**
    - Make changes to the local HelloWorld project.
    - Push the changes to the private GitHub repository.
    - Jenkins will automatically detect the changes and redeploy the project to **VM2**.

14. **Configure Jenkins for Automated Deployment:**
    - Configure Jenkins to periodically check for new releases on the master branch of the GitHub repository and deploy changes automatically if found.

15. **Test Automated Deployment with New Releases:**
    - Push changes to the master branch of the GitHub repository.
    - Verify that Jenkins detects the changes and deploys them to **VM2** automatically.

- **Documentation Tasks:**
  - Create a step-by-step guide for setting up Jenkins and configuring the CI/CD pipeline.
  - Provide troubleshooting tips for common issues encountered during Jenkins setup and deployment.
- **Delivery Report:**
  - Prepare a summary of the CI/CD pipeline setup, including screenshots of Jenkins configurations and successful deployments.
  - Include a troubleshooting guide for common setup issues related to Jenkins and GitHub integration.

---
