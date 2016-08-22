__Read below__


Here is a link to my github with changes I added for the docs: https://github.com/lamarwhitej/rst/blob/master/BaremetalDoc.md

It is a bit nitpicky some of it. So don't pay it too much mind.  For some areas I went in and added the changes I wanted.  
For those areas I didn't add them to the docs (except typos).  I just added it manually.

Those changes are only in the OSA install though. __Search "Ala" in OSA doc__.  And you will see what I added.
For the baremetal I just had suggestions and typos.  They can be found below.

Also, note the links I added in here are just reference points to where in the doc.

===

__FIRST DOC BAREMETAL__

Read Initial Instructions
=========================
Started 12:00
- steps for installing f5 vpn to the browser
  * it installed for us automatically through the browser but initially we thought we needed to go download something
- What is iLO?
- For section 1, you should specify that as long as you have the browser up and logged in you are connected to the OSIC VPN.

Time 10 mins


Deployment Host Doc
===================
Start 12:10
- In step 5 of "Manually provision the deployment host" why are we adding this preseed url?
  This may need to be noted.

End 1:46
Time 1hr 36mins (forgot to uncheck box for image)

Cobbler - Setup the osic-prep LXC Container
==========================================
Start 1:46
- In 'Cobbler Overview' section, would need to be --among other things--. I changed it in the my link already.

PxE Boot SErvers
================
2:20
- after creating csv it states 'after running the next command' should after running the next script. I started looking for a command. I added this in my link already.
https://github.com/lamarwhitej/rst/blob/master/BaremetalDoc.md#create-input-csv


finished at 3:30

Bootstrapping the Servers
=========================
10:35
- What is bootstrapping?
  Because I felt that we already assigned the IP addresses earlier which all I assumed bootstrapping was.
- Why did we need to add hosts to known hosts for the container?? Is this to bypass prompts and create a silent login?
- Should say what to do (or how far back to go to retry) in case of failure.
   vvvv didn't help much
- add note for user that if they stop for a period of time during installation the servers may lose their IPs and require restarting to gain them back from dhcp
- Also add a part for at what point you can stop and not suffer consequences in case the user needs to leave for the day or something
- Add start back points after errors or failures.  Like it errors here go back to step xyz
- Please add that in ilo.csv file you can/should change the names to be more user friendly (or it may cause problems)

- for this step what password? I know what it is but you should add it.  I added it in the link
  https://github.com/osic/ref-impl/blob/master/documents/bare_metal_provisioning.md#bootstrap-the-servers

- At step below directions say that you can "quickly" add this but the screen was still for about 10 seconds.  I thought something was wrong. Should add that screen will be still for a moment
  https://github.com/osic/ref-impl/blob/master/documents/bare_metal_provisioning.md#update-linux-kernel-1

End 12:51


===

__Second DOC OSA__

OSA INSTALL
===========
Begin 12:55
Intro - Prepare Deployment Hosts
======
- Check bullet points.  What is "Three logging hostsm". I fixed it in my doc.
https://github.com/osic/ref-impl/blob/master/documents/osa-refimpl-deploy.md#intro

Prepare Target Host
=================================
Begin 1:07
- typo "First, Determine". I fixed it in my doc.
https://github.com/osic/ref-impl/blob/master/documents/osa-refimpl-deploy.md#setting-up-storage-devices

- No reference to what pxe_network should be. They will more than likely already know.  But just a, and you know what pxe should be or something
https://github.com/osic/ref-impl/blob/master/documents/osa-refimpl-deploy.md#configure-network-for-target-hosts-deployment-included

end 1:31

Configuring OpenStack environment
=================================
Messed up a lot here. So times got off.
- Should I add the other 2 infra hosts for loadbalancer?? On step 2.  That isn't mentioned.
https://github.com/osic/ref-impl/blob/master/documents/osa-refimpl-deploy.md#configuring-openstack-environment


Openstack Installation
======================

- Adding how long running scripts will be if it is more than 30 seconds will help
https://github.com/osic/ref-impl/blob/master/documents/osa-refimpl-deploy.md#openstack-installation
