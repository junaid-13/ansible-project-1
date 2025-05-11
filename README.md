# Ansible Project to set up work station

## Features
- Create developer user accounts
- Install essential software packages (`git`, `curl`, `htop`)
- Set custom Message of the Day (MOTD)
- Configure system hostname
- Set timezone to UTC

## Project Structure
- /work.yaml
- /README.md

## Usage
1. **Clone the repository**
   ```bash
   git clone https://github.com/junaid-13/ansible-project-1.git
   cd ansible-project-1```
   
2. **Configure the host file**
  -  ```bash
      cd /etc/ansible
      sudo vi hosts```

   - ```bash
     [myhost] #you can change the myhost with your own
     12.34.214.23 ansible_user=USER ansible_ssh_private_key_file= PATH # You can change this Ip address with your respective ip address, change the username and path as per your username and Path of your private key file(pem file)
     ```
  - Press :wq! and enter on your key board and it will exit from your vim editor

    
3. **Run the playbook**
    ```bash
    ansible-playbook work.yaml``` 
    
            or 

    ```bash
    ansible-playbook work.yaml --list myhost```
