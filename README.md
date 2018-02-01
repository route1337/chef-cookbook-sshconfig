Chef Cookbook - r1337-sshconfig
==============
This Chef cookbook will configure SSH on Linux servers to be compliant with Route 1337 security policies. There are a few versions of the configuration depending on the recipe that is chosen

SSH Config Recipes
------------
1. standardssh.rb is the standard recipe suitable for use on internal LANs or where networks are trusted to be secured
2. hardenedssh.rb is a recipe for use in DMZs or other networks where sophisticated attacks are either expected, or where more stringent policies exist

Changes Performed
------------
1. Configures OpenSSH server with custom security settings depending on recipe selected.
2. Ensures OpenSSH is installed, configured and enabled/running

Requirements
------------
1. Chef (Tested on Chef 13)
2. Linux chef-clients (Tested on Ubuntu 14.04, Ubuntu 16.04 and CentOS 7.2 but kitchen will let you test anything you want)
3. The openssh cookbook from Chef Supermarket


Installation Tips
------------

1. I personally use Berks to install this into my Chef server, because it's easier.
2. You must set the attribute ['r1337-sshconfig']['sshpolicy'] to `hardened` if you want something stronger than the default. For most people the default is fine.

Limitations
------------
1. None so far :)

Known Issues
------------
1. None so far :)

Bug Fixes & Changes
------------

1. v0.1.1
    1. TODO
2. v0.1.0
    1. Initial release

Use Cases
------------
Configuring SSH as part of a base security requirement
