This is a base Linux image (Ubuntu 18.04) that can be used for doing your
course work throughout the semester. It has all the required libraries and
tools already installed.

To use the base image you will need to install two tools - Vagrant and
VirtualBox. To install Vagrant please refer the instructions shown on this
page: https://www.vagrantup.com/downloads.html. Next install VirtualBox by
going to this link: https://www.virtualbox.org/wiki/Downloads.

To use the VM, clone the base image repository by running the following command

```
git clone <link_to_repo>
```

Go to the new cloned directory and run the following command

```
vagrant up
```

This should bring up VirtualBox with the base image running within it.
