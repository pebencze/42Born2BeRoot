# Born2beRoot

## Project Overview

The Born2beRoot project introduced me to the fundamentals of system administration and virtualization. I created a virtual machine using VirtualBox and set up a server with specific configurations and security measures. This project will enhanced my understanding of operating systems, server management, and virtualization technologies.

## Features

In this project:

    Virtual Machine Setup:
    
        I used VirtualBox or UTM to create a virtual machine.
        Chose either the latest stable version of Debian or Rocky Linux (Debian recommended for beginners).

    Server Configuration:
    
        No graphical interface was allowed (no X.org or equivalent).
        Installed and configured SSH to run on port 4242, disallowing root login.
        Configured a firewall (UFW for Debian or firewalld for Rocky) to only allow traffic on port 4242.
        Set the hostname to my login ending with "42" (e.g., pbencze42).
        Implemented a strong password policy.
        Configured sudo with strict rules, including custom error messages and logging of sudo commands.

    Disk and Partitioning:
    
        Created at least two encrypted partitions using LVM.

    Monitoring Script:
    
        Developed a monitoring.sh script in bash that displays system information (e.g., CPU usage, memory usage) every 10 minutes on all terminals.

Submission

    Only a signature.txt file is required at the root of the repository. This file should contain the SHA-1 signature of the virtual machine’s virtual disk.

Commands to Get Signature

    Windows: certUtil -hashfile your_vm.vdi sha1
    Linux: sha1sum your_vm.vdi
    Mac M1: shasum your_vm.utm/Images/disk-0.qcow2
    MacOS: shasum your_vm.vdi

Example output:

    6e657c4619944be17df3c31faa030c25e43e40af
