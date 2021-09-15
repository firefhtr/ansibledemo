![SUSE Manager Logo](/images/susemanagericon.jpg)

![https://www.suse.com/products/suse-manager/](url)
# Small Ansible playbook demo for SUSE Manager


## Background:

This repository contains some sample Ansible playbooks that can be used for a SUSE Manager Lab for 
learning or a quick demo.
 
Note at the this time, this feature within SUSE Manager is marked as Tech Preview.

## Setting up the environment:

You will need the following devices in your lab:
    1. One ControlNode - I used SLES15-SP3 as the base Operating System. The ansible package will be provided 
       from the SUSE Manager tools channel.
    2. At least one (1) target device, in my lab I have setup up 3,  1 device for each of the 
       following Operating Systems: SLES15 Sp3, CentOS 7 and Ubuntu 18.04.

## Device requirements:

The ControlNode must be able to ssh as Root to each target device without password (ssh-copy-id).

## File Location:

This is dealers choice as you will be setting the location of both the playbooks and inventory files
within SUSE Manager.  

All devices must be registered to SUSE Manager. You can jst register the ControlNode, but if there 
are any packages to be installed as part of the playbook, then the devices will have to have
access to those packages via their own repositories.  This can create unknown issues as version
maybe different.

## Playbooks:

The playbooks in this repository is split amongst the different directories based on environment and
OS versions with the exception of the directory called 'general'.  This directory is design to show 
the ability to deploy a single playbook across different Operating Systems.

Good luck