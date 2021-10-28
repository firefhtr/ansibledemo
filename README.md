![SUSE Manager Logo](/images/susemanagericon.jpg)

![https://www.suse.com/products/suse-manager/](url)
# Small Ansible playbook demo for SUSE Manager 4.2

## Background:

This repository contains some sample Ansible playbooks that can be used for a SUSE Manager 4.2 Lab for 
learning or a quick demo.
 
Note at the this time, this feature within SUSE Manager 4.2 is marked as Tech Preview.

## Setting up the environment:

You will need the following devices in your lab:
    1. One ControlNode - I used SLES15-SP3 as the base Operating System. The ansible package will be provided 
       from the SUSE Manager tools channel.
    2. At least one (1) target device, in my lab I have setup up 4,  2 device for each of the 
       following Operating Systems: SLES15 Sp3 and CentOS 7

## Device requirements:

The ControlNode must be able to ssh as Root to each target device without password (ssh-copy-id).

## File Location:

This is dealers choice as you will be setting the location of both the playbooks and inventory files
within SUSE Manager.  

All devices must be registered to SUSE Manager. You can just register the ControlNode, but if there 
are any packages to be installed as part of the playbook, then the devices will have to have
access to those packages via their own repositories.  This can create unknown issues as version
maybe different.

## Playbooks:

The playbooks in this repository is split amongst the different directories based on environment and
OS versions with the exception of the directory called 'general'.  This directory is design to show 
the ability to deploy a single playbook across different Operating Systems.

## Getting Started:
Now that your environment is setup, here is a link to the documentation on how to setup this up in 
SUSE Manager ![https://documentation.suse.com/suma/4.2/en/suse-manager/administration/ansible-integration.html](url)

You will also find sample salt states as a comparison.

Good luck