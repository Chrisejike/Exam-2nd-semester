

# Segments

* Ansible playbook containing - 
    1. Ansible.cfg file tha holds configuration of ansible,
    2. Inventory - Holds the target machine's IP address
    3. Site.yaml - Copies the cron job, copies the laravel file, changes the command on the file and runs the laravel script.

* Laravel-slave.sh file - Installs and deploys the laravel application with LAMP stack.

* Master-slave.sh file - Generates master and slave machines.

* Laravel.sh - Deploys Laravel on the master machine.




# How to run the script

1. Spin up the master and slave machines
![1.spin up](./screenshots/1.%20spin%20up%20master%20and%20slave%20machines.png)


2. SSH into the master machine, enter as a root user and run laravel.sh script
    - update and upgrade server
    - install LAMP stack
    - install composer
    - configure apache2
    - clone laravel
    - configure mysql
    - execute key gen and migrate for php

![1.SSH into master](./screenshots/2a.%20ssh%20into%20the%20master%20machine.png)
![2b.Run laravel.sh](./screenshots/2b.%20run%20laravel.sh.png)
![2c.Run laravel](./screenshots/2c.%20run%20laravel.png)


    


3. SSH key gen and generate key pair.
![3. Ssh key gen](./screenshots/3.%20ssh%20key%20gen%20and%20pair.png)

4. Run ansible playbook to
    - update and upgrade server,
    - set cron job to check uptime of server,
    - copy bash script to slave machine,
    - set execute permissions on script,
    - run bash script.
![4. Run ansible play book](./screenshots/4a.%20run%20ansible.png)

5. Further screen shot evidence
![5. Further screen shots](./screenshots/5.%20Further%20screen%20shots.png

6. Functional php app via VM IP address
![6. Functional php app via VM IP address](./screenshots/6.%20Functional%20php%20app%20via%20VM%20IP%20address.png)
