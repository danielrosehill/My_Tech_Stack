# My Personal Technology Stack

I created this repository to host a periodically-updated list of my favorite tech products spanning pretty much all domains of use. I figure this might save me a bit of time in representing (mostly) the same products to friends, colleagues, etc.

*(Latest updated: 01/04/24 or last commit ... whichever is later!)*



## My OS: Ubuntu Linux (LTS)

**Ubuntu Linux (LTS releases)**

I've been using Linux as my day to day OS for more than 15 years.

I've spent my fair share of time distro-hopping and have run Debian, Gentoo, Arch (among others) at different times.

But over time I've come to prefer a reliable LTS Ubuntu distro as the backbone of my system.

After one too many bad updates I've learned to stick to the LTS release cycle. 

## Virtualization (Desktop): VMWare Workstation.

I'm just about old enough to remember the "bad old days" when emulators like WINE were just about the best hope for us Linux weirdos to be able to interface with the normal folk running Windows/MacOS.

![image-20240408170614275](images/image-20240408170614275.png)

I switched from using **Openbox** to VMWare a few years ago and haven't looked back since. I find Genymotion useful too for the few times I need/want to emulate Android on Ubuntu.

I recently upgraded from VMWare Player (freeware) to VMWare Workstation Player (license-based). My rationale for doing so was that snapshotting, cloning, and moving Windows VMs is easier with Workstation. The Linux client is perfectly good.



## Desktop Environment: LXDE (Yes, Still!)

## **LXDE**

When I started using Linux I was a poor university student without a lot of disposable income.

LXDE allowed me to run Ubuntu on old hardware as if it were brand spanking new! Even though I finally own a desktop computer with some decent firepower in it, I've been using LXDE for so long that it's an impossible habit to break!

I played around with tiling window managers for a period (they're cool). But I think that LXDE strikes a happy medium between usability and minimalism (every time I use Windows or even Unity I'm blown away by how bloated the DEs are with graphic effects and the like)

## To Do: Ansible 

I hate when I have a tech problem that I know there's a solution to but which I really don't have time to implement. Thus it is with me and Ansible.

I spend 95%+ of my computing time using a Linux desktop but I like to keep an Ubuntu laptop somewhat in sync so that I don't get an old config when I use it.  

I've looked into various ways to do this both intelligently and easily but have thus far come up short

Ansible or some other automation solution has been on my to-do list for ages.



## Computer & Hardware: Desktop Built By People-Who-Know-What-They're-Doing (Ie, Not Me)

Desktop or laptop?

Desktop  each and every day!

I use my laptop only when I'm travelling.

I've also been a longtime user of three horizontal displays. 

This is the monitor array that I've had the best success with for general productivity. 

I've tried both more and less and found that 3 is my personal sweet spot.



<img src="images/desktop.png" alt="desktop" width="500" alight="left"/>

Multimonitor support on Ubuntu works out of the box these days and you can set up far more elaborate arrays than my relatively simple layout.

I use **arandr** for configuring the layout. Once I've figured out the right parameters I save that as a Bash script which I execute automatically when I log into the DE.

![](images/arandr.png)

![](images/2.png)



Here in Israel we have an interesting solution for buying desktops that I think would do well just about everywhere there are still desktop fans.

When you want to buy a desktop, you consult with a "tech guy" and together select the components. 

As a Linux user, I even save a little by avoiding wasting money on a Windows OS license that I'm not going to need! Both KSP and Ivory offer this sales model and it's how I've bought the two desktops I've owned to date (the current machine I'm typing this with and my previous computer).

I think it's an amazing happy medium between building your own computer (lots of work) and getting stuck with an off the shelf commercial build that's not going to contain exactly the components you want. 

## Proxmox

Although I make extensive use of Reddit for exploring its many excellent tech communities, I remain averse to describing my home computer and networking setup as a "homelab", I've read the threads explaining what it means but ... it still feels to me like an unnecessary piece of jargon.

![image-20240408171331317](images/image-20240408171331317.png)

One software that's popular among HomeLab-ers and which I love, however, is Proxmox. 

Proxmox has made it massively easier for me to mess around with VMs and Containers and ... explore tech more deeply in general.

Currently I'm hosting Proxmox on an Aliexpress mini PC that was originally purchased with the hope that it could be a nice networking appliance to bond up Speedify connections and serve them to the network. 

Fiber optic internet arrived before I figured out how to do that so it's been repurposed. I'll probably set up a new cluster on an old desktop.

![Inventory20240313_154500](images/Inventory20240313_154500.jpg)

## NAS: Synology



Another piece of hardware that I get a lot of mileage out of is my Synology NAS. I've tried out TrueNAS and other platforms before but *mostly* actually prefer the Synology. 

Before discovering Proxmox, I hosted some VMs and container on it with less than amazing performance. I've reverted to using it as a big dedicated backup appliance. I move backups onto it and sync backups up to and down from various clouds.



![Inventory20240408_171814](images/Inventory20240408_171814.png)

## Backup and Recovery Software

I've documented a lot of my backup approach here on Github. 

But to cut to the essentials.

For backing up my Linux OS:

- **Timeshift** is a great utility for creating convenient system restore points allowing you to quickly roll back the filesystem if you (or a package) messes something up. But it's not wise to consider it a bone fide backup tool (for one, it's typically run on the same physical hardware as the machine you're protecting).

For actual backups, I personally feel most comfortable going with block-level disc imaging tools that really try to mop up every last byte of information on the disc.

The two I use frequently are: **Veeam Agent for Linux** and **Clonezilla** (both have plenty of merits.). I try to clone my OS every 3 months.

