## How to Deploy a Simple Website Using Ansible – A Step-by-Step Guide
Have you ever wanted to automate the process of setting up a web server and deploying a website?
With Ansible, you can do it with just one command! In this blog post, we’ll walk through a real Ansible playbook that automatically sets up an Apache web server, installs necessary software, deploys a website, and starts the services — all without manual intervention.

Let’s break down the playbook.

## What Does This Playbook Do?
  This Ansible playbook contains a play which contain 8 tasks:
  1. Installing packages using the yum module ( httpd, php & git)
  2. Since we are not hard coding the httpd port we are assigning the port number as a variable "httpd_port" and using template module adding the conf file to httpd.
  3. Applying a custom Virtal host template on client machine.
  4. Creating a custom document apache document root as mentioned on virtual host entry.
  5. Cloing the website from git to  the client server.
  6. Copying the website contents to the document root created.
  7. Restarting both apache and php services.

