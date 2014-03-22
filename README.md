mkraspbian-chroot
=================

Script for setting-up a Raspbian chroot directory for developing software for the Raspberry Pi 
(http://raspberrypi.org) on your Linux desktop computer.  
The script can also help you bind-mount /dev, /proc and /sys filesystems to enable device 
access and networking inside your chroot, unmount bind-mounts and start a chrooted shell or 
execute a chrooted command.

Usage:
       mkraspbian-chroot
		(with no arguments will create a chroot in the working directory)
       mkraspbian-chroot [workdir] [chroot name] [distribution] [mirror]
		(name, distrib and mirror are not mandatory for they get default values)
       mkraspbian-chroot mount [/path/to/chroot/dir]
       mkraspbian-chroot unmount [/path/to/chroot/dir]
       mkraspbian-chroot chroot [/path/to/chroot/dir] [command] 
		(if [command] is not passed it will default to a bash shell)

Examples:
    When you run mkraspbian-chroot without any arguments a raspbian wheezy
    chroot will be created in your current directory ($PWD). The chroot
    directory will be named 'chroot-raspbian-armhf'.
    If this directory exists you can choose to overwrite or auto-rename it.

    Create a new raspbian wheezy chroot in directory: /home/username/raspi 
	named: wheezy-armhf

		mkraspbian-chroot /home/username/raspi wheezy-armhf wheezy

    Create a
