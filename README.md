## Base image
This is a base Linux image (Ubuntu 18.04) that can be used for doing your
course work throughout the semester. It has all the required libraries and
tools already installed.

Login details are as follows
```
Username: vagrant
Password: vagrant
```

### Dependencies
To use the base image you will need to install two tools - Vagrant and
VirtualBox. To install Vagrant please refer the instructions shown on this
page: https://www.vagrantup.com/downloads.html. Next install VirtualBox by
going to this link: https://www.virtualbox.org/wiki/Downloads.

### Running the VM
To use the VM, clone the base image repository by running the following command

```
git clone https://github.com/CSCI-UA0480-009/base-image.git
```

Go to the new cloned directory and run the following command

```
vagrant up
```

This should bring up VirtualBox with the base image running within it. **All
Vagrant commands should be run from the same directory that has Vagrantfile. In
this case base-image folder.**

When you are not using the VM, you can either suspend or halt the VM using

```
vagrant halt
```
or
```
vagrant suspend
```

To bring the machine back up you can resume a suspended VM by running
```
vagrant resume
```

You can also just say `vagrant up` to bring the machine back up from either
suspended or halted state

## Reprovision VM Image
In the situation when the base image is updated by
course instructors, you will have to reprovision the image on your systems. All
this means is that you have to update the base image with any changes that have
been made. To do this you have to first pull the latest changes from the git
repository by running the following

```
git pull --rebase origin master
```

Once you have the latest changes, close any active instances of the virtual
machine by doing `vagrant halt`. After that run the following command to bring
up the machine with the new changes.

```
vagrant up --provision
```
