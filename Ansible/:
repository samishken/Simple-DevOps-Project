##On RHEL 8.x server

   1 -  Install Python latest version (on Control node and Managed host)

    yum install python3 -y

    2 - By default, python3 is the command to run python commands. to use just python, use "alternatives" command. (on Control node and Managed host)

    alternatives --set python /usr/bin/python3

    3 - Check for Python version

    python --version

    4 - Install python-pip package manager (on Control node)

    yum -y install python3-pip

    5 - Create a new user for ansible administration & grant admin access to the user (on Control node and Managed host)

    useradd ansadmin
    passwd ansadmin

    6 - Below command adds ansadmin to sudoers file. But we strongly recommended using "visudo" command if you are aware vi or nano editor. (on Control node and Managed host)

    echo "ansadmin ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers

    7 - Using key-based authentication is advised. If you are still at the learning stage use password-based authentication (on Control node and Managed host)

    # sed command replaces "PasswordAuthentication no to yes" without editing file 
     sed -ie 's/PasswordAuthentication no/PasswordAuthentication yes/' /etc/ssh/sshd_config
     sudo service sshd reload

    Install Ansible as a ansadmin user (on Control node)

    su - ansadmin
    pip3 install ansible --user

    Note: Ansible must be installed as a user (here ansadmin)

    8 - check for ansible version

    ansible --version

    9 - Log in as a ansadmin user on master and generate ssh key (on Control node)

    ssh-keygen

    10 - Copy keys onto all ansible managed hosts (on Control node)

    ssh-copy-id ansadmin@<target-server>

##Validation test

    1 - Create a directory /etc/ansible and create an inventory file called "hosts" add control node IP address in it.

    2 - Run ansible command as ansadmin user it should be successful (Master)

    ansible all -m ping


