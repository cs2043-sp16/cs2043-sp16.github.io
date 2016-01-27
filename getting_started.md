---
title: Getting Started
layout: main
---

You will need to configure two items:

1. Create and link a GitHub account. This is where assignments will be released, as well
   as submitted.

2. Configure a Unix development environment.  This is needed to complete the assignments.


## GitHub
------------

We will be using GitHub to release assignments, as well as host other materials related
to the course.  You will also be submitting your assignments through GitHub, but to get
started you just need to create your account and link it using the form in (3) below.

1. Create a free <a href="https://github.com/" target="_blank">GitHub</a> account, if
   you do not already have one.  You will need to register it with your official Cornell
   e-mail if you wish to complete step 2.<br />

2. Optional, but encouraged.  Request a <a href="https://education.github.com/pack" target="_blank">
   Student Developer Pack</a> for your newly created account.  Your school-issued e-mail
   is (usually) required for approval.  This step is not necessary for this course, but
   it will enable you to have private repositories for other courses while still adhering
   to the Academic Integrity code.<br />

3. Provide me with with a mapping of your GitHub username to your Cornell NetID
   so that we know who you are on GitHub.  Fill out
   <a href="http://goo.gl/forms/0HkAX4BxjO" target="_blank">this form</a> **after** you
   have created your GitHub account.  You have to be signed into your Cornell e-mail to
   fill out the form.

## Unix Environment
----------------------

To complete the assignments, you will need access to a Unix development environment.  If
you do not already have a native Unix installation, you will need to configure a "Virtual
Machine (VM)."  The short version is that a VM is just another application that your native
operating system runs, where this application is another operating system.  Think
Inception.

### Do I need a Virtual Machine?

Not everybody needs to setup a Virtual Machine.

- If you are running Windows on your computer / tablet, the answer is **yes**.
- If you are running Mac OSX, the answer is **not necessarily**.  Mac OSX *is* a
  Unix-based operating system.  Though I encourage you to configure one so you can
  play with Linux.
- If you are using a Chromebook, then the answer is **most likely not**.
  Unfortunately, I do not have one and cannot confirm or deny.
- If you are running some form of Linux already, then the answer is **no**.

### Configuring the Virtual Machine (VM)

This part will take some time, for no other reason than you have to download some large files.
We will be using VirtualBox, but if you have already paid for a different Virtual Machine
software (e.g. VMWare), you *should* be able to use the `.ova` files I have prepared.  I will
not be able to provide you with instructions for configuring / tailoring this, though.

I have prepared two separate Virtual Machines for you to choose from: Fedora 23, and Ubuntu 15.10.
If you don't want to read any more, just download the Ubuntu 15.10 VM in step 2.  The **Options**
section and below explains a little more about what each choice is.  You only need to choose one,
but if you have a reasonable amount of space on your computer you may want to play with both.

#### Step 1: Install the Tools

Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).

1. First, install the "VirtualBox platform" (this is the application).
2. Next, install the "VirtualBox Extension Pack" (make sure you download the same version of the
    extension pack as you did the platform package).  

###### ATTN: Windows 10 Users

Please download the latest version of VirtualBox from the website linked above (the one that shows
up on the page will work).  Windows 10 is not officially supported until v5.0 and higher.  Installing
a 4.x or lower version can have adverse affects, and can even lead to [BSOD](https://en.wikipedia.org/wiki/Blue_Screen_of_Death).


#### Step 2: Acquire the Virtual Machine

There are three places you can download your VM from, if you are on campus you should try the Cornell
mirrors first as they will be significantly faster.  If you live off campus, I encourage you to go
to campus for this section.  Cornell has *very* fast internet, in comparison to the rest of town.

If you are on Windows, you should compare the number of bytes listed in the size rather than GB.
If they are the same, then you should have received the whole file.  Windows and Unix systems don't
always agree on what a GB actually is.

##### Fedora 23 Hosts

    File: cs2043-fedora.ova
    Size: 2.2 GB (2196170240 bytes)
    MD5:  4cffb9a8e02278c26610c1663d83d748

###### Download Mirrors:
- [Cornell Course Website](http://www.cs.cornell.edu/courses/cs2043/2016sp/vms/cs2043-fedora.ova)
- [Cornell Box](https://cornell.box.com/cs2043-fedora)
- [Google Drive](https://drive.google.com/file/d/0B47IM_slYhMna1FBUjEwSTJwbmc/view?usp=sharing)

##### Ubuntu 15.10 Hosts

    File: cs2043-ubuntu.ova
    Size: 1.88 GB (1876179456 bytes)
    MD5:  a40301eb2f7d621821be0b05a2cf5b9a

###### Download Mirrors
- [Cornell Course Website](http://www.cs.cornell.edu/courses/cs2043/2016sp/vms/cs2043-ubuntu.ova)
- [Cornell Box](https://cornell.box.com/cs2043-ubuntu)
- [Google Drive](https://drive.google.com/file/d/0B47IM_slYhMnYk5mN1piM212NFU/view?usp=sharing)

#### Step 3: Install the Virtual Machine

What you just downloaded is an archive of a Virtual Machine (think of it like a .zip file).  All
you need to do is have VirtualBox extract it.

1. Launch VirtualBox.
2. From the menubar, choose "File->Import Appliance".
3. Navigate to where you downloaded the `.ova` file from step 2 and select it.
4. Click continue.
5. Check the box that says "Reinitialize the MAC address of all network cards."
6. Click import, and let VirtualBox take over.

#### Step 4: Customize the Virtual Machine

The VMs I made have very small demands to allow everybody to use them.  Specifically, they use 1 core and only need 2048MB of RAM.  Many of you will have plenty more available, I will cover in lecture how to configure this a little more.

<em>Video tutorial coming shortly</em>.

### Options

In this day and age there are a **lot** of [different Linux distributions][distros].  Many of
them are very similar, but the list grows out of various special needs for different organizations
and platforms.  In my experience, the two most commonly used "flavors" of Linux are
Debian-based and RPM-based.  From there, the general trend seems to be that

- Most independent developers tend to use Debian-based (typically [Ubuntu][ubuntu]) Linux
  - Ubuntu is a common choice because it has a huge user-base, and therefore a lot of
    community support.
- Corporations tend to use RPM-based Linux.
  - The cause of this is likely because the Enterprise Linux providers such as
    [Red Hat Enterprise Linux (RHEL)][RHEL] and [SUSE Linux Enterprise Server (SLES)][SLES]
    ensure stability and contract support, which gives corporations certain assurances.

As such, I have prepared Virtual Machine for each category.  Ubuntu is the obvious choice for
Debian-based Linux, and I have chosen to provide [Fedora][fedora] as the RPM-based Linux choice.
[This article][red-relations] explains how Fedora, RHEL, and CentOS relate.  I personally develop
in both Mac OSX and Fedora, but I also have Ubuntu and Windows installed for compatibility testing.

[distros]: https://en.wikipedia.org/wiki/List_of_Linux_distributions
[ubuntu]: http://www.ubuntu.com/
[RHEL]: https://www.redhat.com/en/technologies/linux-platforms/enterprise-linux
[SLES]: https://www.suse.com/
[fedora]: https://getfedora.org/
[red-relations]: https://danielmiessler.com/study/fedora_redhat_centos/

### Which one should I choose?

Well, it's up to you...you're more than welcome to try both, but you should not try and run them
both at the same time!!!  Both Virtual Machines should be stable enough for you to give them a
test drive.  If enough interest is demonstrated, we will cover how to install Linux natively on
your computers near the end of the course.  For convenience and ease, though, Virtual Machines
are an effective way to "try before you buy".

- If you want things to "just work", use Ubuntu.  As stated above, this has the widest support.
- If you are feeling adventerous, try Fedora.  This distribution prides itself in being the
  "bleeding edge" -- you will have access to many very new features.  This *does* come at a price,
  as this makes the system less stable.  This will not be as noticeable in Virtual Machine form,
  but must be disclaimed if you intend to install it natively.
