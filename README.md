Vagrant LAMP Stack
=================

Description
-----------

Setup a dev environment using Vagrant and PuPHPet.

INSTALL/SETUP A BASIC LAMP STACK (LINUX, APACHE, MYSQL, PHP) ON UBUNTU 14.04 LTS

Requirements
------------

* [VirtualBox](https://www.virtualbox.org)
* [Vagrant](http://vagrantup.com)
* make sure the directory c:\www exists (This is where we put our projects)
* some patience :)

Installation
------------

Clone the repository:


	$ git clone https://github.com/oussamak/Vagrant-LAMP-Stack.git
	$ cd Vagrant-LAMP-Stack

Then, you should be able to use:


	$ vagrant up


Once everything is done you can log into the virtual machine:


	$ vagrant ssh

How do I update my hosts file?
------------------------------

You will need to open and edit your hosts file with a text editor like notepad, sublime_text, nano, etc. The location of the hosts file varies by operation system.

Windows users could look here: c:\windows\system32\drivers\etc\hosts

Linux and Mac OSX users could look here: /etc/hosts.

Example Entry: 
	
	192.168.56.101 local.dev www.local.dev


Virtual Machine Management
--------------------------

When done just log out with `^D` and suspend the virtual machine

	$ vagrant suspend


then, resume to hack again

	$ vagrant resume


Run

	$ vagrant halt


to shutdown the virtual machine, and

	$ vagrant up


to boot it again.

You can find out the state of a virtual machine anytime by invoking

	$ vagrant status


You can run your own custom code after the VM finishes provisioning by adding files to the **puphpet/files/exec-always**, **puphpet/files/exec-once**, **puphpet/files/startup-always**, and **puphpet/files/startup-once** folders.

Finally, to completely wipe the virtual machine from the disk **destroying all its contents**:

	$ vagrant destroy # DANGER: all is gone


Information
-----------

* Virtual Machine IP: 192.168.56.101
* go to http://local.dev
* PHP 5.6 installed
* User/password: vagrant/vagrant
* MySQL user/password: root/admin
* node, npm (some useful packages: grunt, grunt-cli, yoeman, bower, express, gulp)


Troubleshooting
---------------

### 