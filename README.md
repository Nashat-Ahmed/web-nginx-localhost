# Web Nginx Localhost Project

This project is a web application designed for local hosting with Nginx, featuring multiple HTML pages, assets, and configuration files. It supports containerized deployment with Docker, orchestration with Kubernetes, and automated deployment through Ansible and Jenkins.

## Project Structure

- **Documentation/**: Project-related documentation.
- **assets/**: Static files like CSS, JavaScript, and images.
- **k8s/**: Kubernetes configurations for deployment.
- **src/**: Source files for the web application.
- **Changelog.htm**: Document tracking project changes.
- **Dockerfile**: Used to build the application’s Docker image.
- **Help.htm**: Guide to assist with using the project.
- **Jenkinsfile**: Jenkins pipeline configuration for CI/CD.
- **ansible-playbook.yaml**: Automates deployment tasks with Ansible.
- **inventory**: Ansible inventory file specifying target hosts.
- **vars.yaml**: Variables file for Ansible configurations.

## Key Pages

The web app includes:
- `index.html`: Main landing page.
- `about.html`, `contacts.html`: Information and contact pages.
- `events.html`, `schedule.html`: Event-related pages.
- Additional pages include `teacher-single.html`, `class-single.html`, and blog content pages.

## Setup and Deployment

### Prerequisites
- Docker
- Ansible
- Kubernetes (optional, for cluster deployment)
- Nginx

### Local Setup

### Clonning the repository
 - git clone https://github.com/Nashat-Ahmed/web-nginx-localhost.git
 - cd web-nginx-localhost
   
### Install dependencies
- npm install

### Build and run the Docker container
- docker build -t web-nginx-localhost .
- docker run -d -p 80:80 web-nginx-localhost

### Ansible Deployment:
1- Configure inventory with your server details
2- Run the playbook:
 - ansible-playbook -i inventory ansible-playbook.yaml

### Kubernetes Deployment:
1- Ensure your cluster is set up
2- Apply configurations:
 - kubectl apply -f k8s/

## Jenkins Pipeline
The Jenkins pipeline (Jenkinsfile) builds the Docker image, runs tests, and deploys the application on AWS (EC2 instance) Using Ansible-playbook. 
