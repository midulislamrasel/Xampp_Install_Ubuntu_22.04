# Step 1: Download the installation package

    https://www.apachefriends.org/index.html

# Step 2: Make the installation package executable

###### Move to the Downloads folder by using the following comma

    $ cd /home/[username]/Downloads

###### The installation package you downloaded needs to be made executable before it can be used further. Run the following command for this purpose:

    $ chmod 755 [package name]

### Example:

    $ chmod 755 xampp-linux-*-installer.run

# Step 3: Confirm execute permission

###### It is important to verify if the package can be executed by the current user. The execute permission can be checked through the following command:

    $ ls -l [package name]

### Example:

    $ ls -l xampp-linux-x64-8.1.12-0-installer.run

# Step 4: Launch the Setup Wizard

    $ sudo ./[package name]

### Example:

    sudo ./xampp-linux-x64-8.1.12-0-installer.run

# Step 5: Work through the graphical setup wizard

#### Now that the Setup Wizard for XAMPP by Bitnami is launched as follows, click the Next button to start the installation process:

# Step 6: Launch XAMPP through the Terminal

###### In order to launch XAMPP through your Ubuntu Terminal, enter the following command as root:

    $ sudo /opt/lampp/lampp start

###### In order to install Net Tools, run the following command as root:

    $ sudo apt install net-tools

# Step 7: Verify Installation

###### After you have installed XAMPP on your Ubuntu system, it is good practice to verify the installation. To do so, enter the following URL in your Firefox browser:

    http://localhost

###### You can also verify the installation of phpMyAdmin in a similar manner by entering the following URL in your browser:

    http://localhost/phpmyadmin

# Step 8: Stop / Start XAMPP Server

    $ sudo /opt/lampp/lampp start
    $ sudo /opt/lampp/lampp stop

#

# XAMPP: Starting Apache...fail

#

###### The reason for the message Starting Apache... fail it's because the apache2 service is already running(enabled) while our system starts. We can check that using:

        $ sudo systemctl status apache2

#### These two commands will solve the problem but NOT permanently.

    $ sudo /etc/init.d/apache2 stop
    $ sudo /opt/lampp/lampp start

#### We can disable the apache2 service so that it won't start everytime we boot our system:

    $ sudo systemctl disable apache2

###### This will solve the issue but I'm not sure if disabling a service is a good idea.

#

# Welcome to phpMyAdmin Error

#

    $ sudo /etc/init.d/mysql stop
    $ sudo /opt/lampp/lampp restart


# Xampp Control Panel
If you use a 32-bit system:
sudo /opt/lampp/manager-linux.run

If you use a 64-bit system:
sudo /opt/lampp/manager-linux-x64.run

###Srvice apache2 stop comment
sudo service apache2 stop
