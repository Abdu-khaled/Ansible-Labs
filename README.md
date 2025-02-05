
# Ansible-Labs

This repository contains a collection of Ansible labs organized into three main directories: `Ansible-Day1`, `Ansible-Day2`, and `Ansible-Day3`. Each directory includes files and subdirectories that demonstrate various Ansible concepts, such as playbooks, inventory management, variables, loops, conditionals, roles, and more. Below is a detailed breakdown of the contents.

---

## Ansible-Day1

This directory contains files for setting up and configuring an Ansible environment. It serves as an introduction to Ansible basics.

### Files

1. **Dockerfile**  
   - Instructions to build a Docker image for the Ansible environment. It includes necessary dependencies and configurations.

2. **ansible.cfg**  
   - The Ansible configuration file. It specifies settings like inventory location and host key checking.

3. **inventory**  
   - Lists the hosts and groups of hosts that Ansible will manage.

4. **playbook.yml**  
   - A playbook containing tasks, handlers, and roles to automate tasks on managed hosts.

### Usage

```sh
# Build the Docker image
docker build -t ansible-env -f Dockerfile .

# Run a container
docker run -it --rm ansible-env

# Execute the playbook
ansible-playbook -i inventory playbook.yml
```

---

## Ansible-Day2

This directory contains subdirectories that demonstrate advanced Ansible concepts, including loops, conditionals, variables, and tags.

### Subdirectories

#### 1. Loops
Demonstrates the use of loops in Ansible playbooks.

```sh
ansible-playbook -i inventory playbook.yml
```

#### 2. Tags
Demonstrates the use of tags for selective task execution.

```sh
ansible-playbook -i inventory playbook.yml --tags "your_tag"
```

#### 3. Variable-Register
Demonstrates the use of variables and the `register` module.

```sh
ansible-playbook -i inventory playbook.yml
```

#### 4. Variables
Demonstrates the use of variables in Ansible.

```sh
ansible-playbook -i inventory playbook.yml
```

#### 5. When
Demonstrates the use of the `when` conditional in Ansible.

```sh
ansible-playbook -i inventory playbook.yml
```

---

## Ansible-Day3

This directory contains an Ansible role named `web` that demonstrates how to automate the setup and configuration of **NGINX** on **Ubuntu**. The role includes tasks for installing NGINX, copying files using templates, and using handlers to restart the service.

### Files

1. **web/**  
   - The `web` role directory contains all the necessary files and subdirectories for the role.

2. **site.yml**  
   - The playbook that uses the `web` role to configure NGINX.

### Role: web

The `web` role performs the following tasks:

- **Installs NGINX**: Uses the `apt` module to install the NGINX package.
- **Copies a File Using a Template**: Renders a template (`index.html.j2`) and copies it to the NGINX web root directory (`/var/www/html/index.html`).
- **Copies a List of Files**: Uses a loop to copy multiple files to the NGINX web root directory.
- **Restarts NGINX**: Uses handlers to restart the NGINX service when changes are made.

### Usage

```sh
# Run the playbook
ansible-playbook -i inventory site.yml

# Verify the changes
curl http://localhost
```

---

## General Usage

To use any of the playbooks or configurations in this repository:

```sh
# Build the Docker image
docker build -t ansible-env -f Dockerfile .

# Run a container
docker run -it --rm ansible-env

# Execute the playbook
ansible-playbook -i inventory site.yml
```

---

Feel free to explore and modify the files to suit your needs. Happy automating with Ansible! 🚀


--- 

License

This project is licensed under the MIT License.
