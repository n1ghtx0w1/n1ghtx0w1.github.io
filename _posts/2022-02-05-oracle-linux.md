---
title: Getting Started With Oracle Linux
author:
  name: Robert Head
  link: https://github.com/n1ghtx0w1
date: 2022-02-05 21:00:00 -0600
categories: [Education, Linux]
tags: [getting started with oracle linux, oracle, linux, virtualbox, vm, iso, download, install, setup, learn]
image:
  src: https://devclass.com/wp-content/uploads/2018/12/Oracle.jpg
  width: 1000   # in pixels
  height: 400   # in pixels
  alt: Oracle Linux
---

# Getting started with **Oracle Linux** 
[Oracle] | [ISO Download] | [Virtualbox Download]

**Below, you will find a detailed walkthrough installation of Oracle Linux in Virtualbox.  This was done using VirtualBox version 6.1.32, and Oracle Linux 8.5 on February 4, 2022. Please [email] me with any questions, concerns, or feedback.** 

`Please note:` *this was written with absolute beginners in mind*.

## Start by downloading the tools

Locate the appropriate Oracle Linux ISO, [ISO Download], for your setup.

Download the latest [Virtualbox Download] binary. _**(Skip if you already have Virtualbox)**_

Install Virtualbox _**(Again, skip if you already have)**_

---

## Install Oracle Linux in VirtualBox

You'll want to begin by opening up Virtualbox.  Click **new** as outlined with a *red circle* below.

<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/1.png" alt="linux" width="600" height="300"/> 
</p>
<br />

I'll be using **Expert Mode** in this installation.

---

## Name and Operating System
- **Name:** Oracle
    - Name this whatever you like
- **Machine Folder:** D:\VMs
    - Store your virtual machine in a location that has available space.  In my situation I use a dedicated solid state drive for virtual machines, which is, my D:\ is in this scenario.
- **Type:** Linux
    - This is a Linux distro
- **Version:** Oracle(64-bit)
    - This will work if you select other choices; however, Oracle is the version so I do suggest using it.

**Memory Size**
- Select the amount of memory you are able to dedicate to the virtual machine.  In my case I've selected **8192 mb** which is about *8gb* of memory.

**Hard Disk**
- For the purpose of this walkthrough, I am, *creating a new virtual disk*.

Click **Create** as outlined in red below.


<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/2.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Create Virtual Hard Disk

**File Location:**
- Ensure this matches the location you would like to store the `virtual disk`.

**File Size:**
- Set the amount that you are able to allocate to your virtual machine.
    - I selected to use 200gb, but this is for my own use case. **Don't** let this determine your selection.

**Hard Disk File Type**
- I'm using **VDI**
    - *This may vary for your use case. Refer to documentation regarding questions/concerns*.

**Storage on physical hard disk**
- I'll be using **Dynamically Allocated**
    - If you have a use case for *Fixed Size* then use that.

Continue by clicking by clicking **Create** after reviewing the information, and ensuring the settings to be satisfactory.

<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/3.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Settings

Clicking the gear icon with *"Settings"* under, circled in the photo below in red, will open up the settings of your virtual machine.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/4.png" alt="linux" width="600" height="300"/> 
</p>
<br />

## System
We'll start with going into **System** as circled in the image below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/5.png" alt="linux" width="600" height="300"/> 
</p>
<br />

I like to uncheck the floppy and move it to the bottom of the boot order.  It's really just a preference, and not necessary.

Ensure the memory is what you set earlier, or modify it here while in the **Motherboard** tab.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/7.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Next navigate over to the **Processor** tab, as seen below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/8.png" alt="linux" width="600" height="300"/> 
</p>
<br />

I'm able to allocate 4 cores to this virtual machine. You will need to decide on what **CPU** resources to allocate to your virtual machine.  Please read the documentation regarding any questions or concerns here [Oracle]. I make no changes to the execution cap for my use case, and leave the extended features on default settings. If your default settings are different, again, please visit Oracle to locate settings partiuclar to your environment.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/9.png" alt="linux" width="600" height="300"/> 
</p>
<br />

## Display 
Next we'll navigate over to the **Display** settings, which I’ve circled in red below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/10.png" alt="linux" width="600" height="300"/> 
</p>
<br />

**Screen**
- Video Memory
    - I set it to maximum, but you need to determine the graphic memory resources you wish to allocate.
- Monitor Count
    - I have dual displays, but only utilize 1 for my virtual machine.  Set this accordingly.
- Scale Factor
    - `no changes`
- Graphics Controller
    - You may consider changing this option.
- Acceleration
    - You could enable 3d acceleration.

Remote Display
- `no changes`

Recording
- `no changes`

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/11.png" alt="linux" width="600" height="300"/> 
</p>
<br />

## Storage

- Controller IDE

- Controller SATA

- Attributes

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/12.png" alt="linux" width="600" height="300"/> 
</p>
<br />

**Controller IDE**

- Empty Disc
    - Click the empty disc icon to highlight the item as seen below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/13.png" alt="linux" width="600" height="300"/> 
</p>
<br />

- Attributes
    - Select the disc icon to insert the ISO image you downloaded from [Iso Download].
        - Use the drop down menu to navigate to the location where you saved the ISO image.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/14.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You should observe the ISO image populated into the **Controller IDE** now.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/15.png" alt="linux" width="600" height="300"/> 
</p>
<br />

## Network

You may need to adjust this, but remember **wifi** will not be accessible using Oracle Linux by default.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/16.png" alt="linux" width="600" height="300"/> 
</p>
<br />

From here I will select **General** on the left, and **Ok** at the bottom to conclude my initial settings.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/18.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Start Installation Process

Click **Start** at the top to start the virtual machine, and begin our installation process.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/19.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Install Oracle Linux 8.5.0

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/20.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You should see the installer initialize.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/21.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Welcome to Oracle Linux

Select your language, and **Continue** as circled in the image below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/22.png" alt="linux" width="600" height="300"/> 
</p>
<br />

**Installation Summary**

We'll navigate some of these options to set up for our use case.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/23.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Starting here with **Root Password**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/24.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Make sure to create a strong password.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/25.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Next **Software Selection**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/26.png" alt="linux" width="600" height="300"/> 
</p>
<br />

For testing purposes I'm just doing **workstation**, but feel free to experiment and use what you may want to test software wise here. There are lots of selections to choose from.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/27.png" alt="linux" width="600" height="300"/> 
</p>
<br />

After making your selections, select **Done** as shown in the image below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/29.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Then onto **Installation Destination**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/30.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You'll want to make sure that the hard disk selected is blue and has the **check** mark as seen in the image below.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/31.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Then select **Done**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/32.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Next navigate over to **Security Policy**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/33.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Here you can select a **security policy**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/34.png" alt="linux" width="600" height="300"/> 
</p>
<br />

For now I will select **OFF** at **Apply security policy**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/35.png" alt="linux" width="600" height="300"/> 
</p>
<br />

`Important` Network, by default, will not automatically connect to ethernet if you do not select this option and enable it.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/36.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Make sure to enable this option circled below by selecting **ON** for ethernet.  If you do not do this you will need to do it after installation, or manually connect each time.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/37.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Then select **Done**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/38.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Begin Installation

It's time to begin the installation, when you are done going through the selections, and setting up.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/39.png" alt="linux" width="600" height="300"/> 
</p>
<br />

This will take some time depending on the choices you made prior. You will want to click **Reboot System** as circled below, when the **Installation Progress** is complete.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/40.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You'll have the following selections after the system reboot:
- Licensing
    - License Information
- User Settings
    - User Creation

We'll go into **Licensing** first.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/41.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You'll need to accept the agreement before proceeding. You may wish to read the licensing here as well.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/42.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Select **Done** to exit the licensing.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/43.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Next we will select **User Creation**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/44.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Setup your user credentials here.  I'm making this user an **administrator** for testing purposes. I've also selected to **require password** for this user. 

Select **Done** as circled below when finished.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/45.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Now **Finish Configuration**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/46.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

## Login

Login with the user you created.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/47.png" alt="linux" width="600" height="300"/> 
</p>
<br />

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/48.png" alt="linux" width="600" height="300"/> 
</p>
<br />

You should be greeted by the desktop environment, if you selected a *GUI* install environment.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/49.png" alt="linux" width="600" height="300"/> 
</p>
<br />

The gnome-initial-setup may also appear depending on your choices.  

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/50.png" alt="linux" width="600" height="300"/> 
</p>
<br />

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/51.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Highlighted in **yellow** here, I show that, I turn off location services. This is something you need to decide for your own use case. What I am doing does not require this feature.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/52.png" alt="linux" width="600" height="300"/> 
</p>
<br />

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/53.png" alt="linux" width="600" height="300"/> 
</p>
<br />

After selecting your options you are done, and ready to further use Oracle Linux.  

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/54.png" alt="linux" width="600" height="300"/> 
</p>
<br />

Oracle Linux provides **Getting Started Videos**. This content can later be found in **Help**.

<br />
<p align="center">
<img src="https://raw.githubusercontent.com/n1ghtx0w1/oracle-linux/main/assets/img/55.png" alt="linux" width="600" height="300"/> 
</p>
<br />

---

[Oracle]: https://www.oracle.com/linux/
[ISO Download]: https://yum.oracle.com/oracle-linux-isos.html
[Virtualbox Download]: https://www.virtualbox.org/wiki/Downloads
[email]: mailto:attacktheosi@gmail.com

