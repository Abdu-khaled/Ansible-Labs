
# Ansible-Labs

This repository contains a collection of Ansible labs organized into two main directories: `Ansible-Day1` and `Ansible-Day2`. Each directory includes files and subdirectories that demonstrate various Ansible concepts, such as playbooks, inventory management, variables, loops, conditionals, and more. Below is a detailed breakdown of the contents.

---

## Ansible-Day1

This directory contains files for setting up and configuring an Ansible environment. It serves as an introduction to Ansible basics.

### Files

1. **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/Dockerfile)**  
   - Instructions to build a Docker image for the Ansible environment. It includes necessary dependencies and configurations.

2. **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/ansible.cfg)**  
   - The Ansible configuration file. It specifies settings like inventory location and host key checking.

3. **[ansible1.png](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/ansible1.png)**  
   - An image file used for documentation or presentation purposes.

4. **[index.html](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/index.html)**  
   - A simple HTML file, possibly used for displaying information or as part of a web interface.

5. **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/inventory)**  
   - Lists the hosts and groups of hosts that Ansible will manage.

6. **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day1/playbook.yml)**  
   - A playbook containing tasks, handlers, and roles to automate tasks on managed hosts.

### Usage

1. Build the Docker image:
   ```sh
   docker build -t ansible-env -f Dockerfile .
   ```

2. Run a container:
   ```sh
   docker run -it --rm ansible-env
   ```

3. Execute the playbook:
   ```sh
   ansible-playbook -i inventory playbook.yml
   ```

---

## Ansible-Day2

This directory contains subdirectories that demonstrate advanced Ansible concepts, including loops, conditionals, variables, and tags.

### Subdirectories

#### 1. **Loops**
   Demonstrates the use of loops in Ansible playbooks.

   - **Files:**
     - **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Loops/Dockerfile)**: Instructions to build the Docker image.
     - **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Loops/ansible.cfg)**: Ansible configuration file.
     - **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Loops/inventory)**: Lists managed hosts.
     - **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Loops/playbook.yml)**: Demonstrates looping over lists.
     - **[playbook2.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Loops/playbook2.yml)**: Additional examples of loops.
     - **[screenshot/](https://github.com/Abdu-khaled/Ansible-Labs/tree/main/Ansible-Day2/Loops/screenshot)**: Contains visual examples.

   - **Usage:**
     ```sh
     ansible-playbook -i inventory playbook.yml
     ```

#### 2. **Tags**
   Demonstrates the use of tags for selective task execution.

   - **Files:**
     - **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Tags/Dockerfile)**: Instructions to build the Docker image.
     - **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Tags/ansible.cfg)**: Ansible configuration file.
     - **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Tags/inventory)**: Lists managed hosts.
     - **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Tags/playbook.yml)**: Demonstrates tagged tasks.
     - **[A-1.png](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Tags/A-1.png)**: Visual representation of tags.

   - **Usage:**
     ```sh
     ansible-playbook -i inventory playbook.yml --tags "your_tag"
     ```

#### 3. **Variable-Register**
   Demonstrates the use of variables and the `register` module.

   - **Files:**
     - **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variable-Register/Dockerfile)**: Instructions to build the Docker image.
     - **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variable-Register/ansible.cfg)**: Ansible configuration file.
     - **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variable-Register/inventory)**: Lists managed hosts.
     - **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variable-Register/playbook.yml)**: Demonstrates variables and `register`.
     - **[A-5.png](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variable-Register/A-5.png)**: Visual representation.

   - **Usage:**
     ```sh
     ansible-playbook -i inventory playbook.yml
     ```

#### 4. **Variables**
   Demonstrates the use of variables in Ansible.

   - **Files:**
     - **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variables/Dockerfile)**: Instructions to build the Docker image.
     - **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variables/ansible.cfg)**: Ansible configuration file.
     - **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variables/inventory)**: Lists managed hosts.
     - **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variables/playbook.yml)**: Demonstrates basic variable usage.
     - **[playbook2.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/Variables/playbook2.yml)**: Advanced variable usage.
     - **[screenshot/](https://github.com/Abdu-khaled/Ansible-Labs/tree/main/Ansible-Day2/Variables/screenshot)**: Contains visual examples.

   - **Usage:**
     ```sh
     ansible-playbook -i inventory playbook.yml
     ```

#### 5. **When**
   Demonstrates the use of the `when` conditional in Ansible.

   - **Files:**
     - **[Dockerfile](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/When/Dockerfile)**: Instructions to build the Docker image.
     - **[ansible.cfg](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/When/ansible.cfg)**: Ansible configuration file.
     - **[inventory](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/When/inventory)**: Lists managed hosts.
     - **[playbook.yml](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/When/playbook.yml)**: Demonstrates `when` conditionals.
     - **[A-4.png](https://github.com/Abdu-khaled/Ansible-Labs/blob/main/Ansible-Day2/When/A-4.png)**: Visual representation.

   - **Usage:**
     ```sh
     ansible-playbook -i inventory playbook.yml
     ```

---

## General Usage

To use any of the playbooks or configurations in this repository:

1. Build the Docker image:
   ```sh
   docker build -t ansible-env -f Dockerfile .
   ```

2. Run a container:
   ```sh
   docker run -it --rm ansible-env
   ```

3. Execute the playbook:
   ```sh
   ansible-playbook -i inventory playbook.yml
   ```

---

Feel free to explore and modify the files to suit your needs. Happy automating with Ansible!


License

This project is licensed under the MIT License.
