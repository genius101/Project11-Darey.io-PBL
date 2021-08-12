<h1> IN THIS PROJECT WE WOULD WORK ON ANSIBLE CONFIGURATION MANAGEMENT WHERE WE WOULD AUTOMATE PROJECT 7 TO 10</h1>

<p>This Project will make you appreciate DevOps tools even more by making most of the routine tasks automated with Ansible Configuration Management, at the same time you will become confident at writing code using declarative language such as YAML.</p>

<h2>Task</h2>

<p>1. Install and configure Ansible client to act as a Jump Server/Bastion Host</p>

<p>2. Create a simple Ansible playbook to automate servers configuration</p>

<h2>Step 1 - INSTALL AND CONFIGURE ANSIBLE ON EC2 INSTANCE</h2>

<p>Update Name tag on your Jenkins EC2 Instance to Jenkins-Ansible. We will use this server to run playbooks.</p>

![1 a](https://user-images.githubusercontent.com/10243139/129177492-35ccbd24-f6df-4faa-b3a5-a4a4927c0ba5.jpg)

<p>In your GitHub account create a new repository and name it ansible-config-mgt.</p>

![1 b](https://user-images.githubusercontent.com/10243139/129177602-46744844-5717-4b84-93d0-fced92f739fa.jpg)

<p>Instal Ansible</p>

    sudo apt update
    sudo apt install ansible
    
<p>Check your Ansible version by running:</p>
	
    ansible --version
    
![1 d](https://user-images.githubusercontent.com/10243139/129177777-b0c6233d-38a6-45ef-a1d9-a3351a44202e.jpg)

<p>Configure Jenkins build job to save your repository content every time you change it:</p>

<p>Create a new Freestyle project ansible in Jenkins and point it to your ‘ansible-config-mgt’ repository.</p>

![1 e 1](https://user-images.githubusercontent.com/10243139/129178445-c94b8122-3161-44e3-952e-b852d2f978af.jpg)

<p>Configure Webhook in GitHub and set webhook to trigger ansible build.</p>

![1 e 2](https://user-images.githubusercontent.com/10243139/129178503-e4fad420-bade-4194-a27e-895dc2388b36.jpg)

<p>Configure a Post-build job to save all (**) files, like you did it in Project 9.</p>

![1 e 3](https://user-images.githubusercontent.com/10243139/129178576-42a85909-cebb-4f06-a8e2-dad558a2a8f9.jpg)

<p>Test your setup by making some change in README.MD file in master branch and make sure that builds starts automatically and Jenkins saves the files</p>

![1 f](https://user-images.githubusercontent.com/10243139/129178633-26f859c3-af4e-4f53-86e4-3dc3cd38f412.jpg)

<p>Confirm if Jenkins saves the files (build artifacts) in following folder:</p>

	ls /var/lib/jenkins/jobs/ansible/builds/<build_number>/archive/
  
![1 g](https://user-images.githubusercontent.com/10243139/129178725-8bcf12bf-7930-49db-86d5-32fbe31e9c05.jpg)

<h3>Now your setup will look like this:</h3>

![jenkins_ansible](https://user-images.githubusercontent.com/10243139/129178933-eb1f3ac2-e704-41c7-9731-6d0d95cbdfaa.png)

<h2>Step 2 – Prepare your development environment using Visual Studio Code</h2>

<h2>Step 3 - BEGIN ANSIBLE DEVELOPMENT</h2>

- [ ] <p>In your ansible-config-mgt GitHub repository, create a new branch that will be used for development of a new feature.</p>

- [ ] <p>Checkout the newly created feature branch to your local machine and start building your code and directory structure</p>

![3 b](https://user-images.githubusercontent.com/10243139/129180304-7e78178c-bfa1-4c65-8802-a48e9beb3b8d.jpg)

- [ ] <p>Create a directory and name it playbooks – it will be used to store all your playbook files.</p>

- [ ] <p>Create a directory and name it inventory – it will be used to keep your hosts organised.</p>

- [ ] <p>Within the playbooks folder, create your first playbook, and name it common.yml<p>
  
- [ ] <p>Within the inventory folder, create an inventory file (.yml) for each environment (Development, Staging Testing and Production) dev, staging, uat, and prod respectively.</p>

![3 f](https://user-images.githubusercontent.com/10243139/129180519-8fedea0c-de53-4d10-850e-a75d914c88d3.jpg)




