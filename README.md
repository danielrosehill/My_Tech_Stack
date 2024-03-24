# My Personal Technology Stack (Updated ... Sometimes)

I created this repository to host a periodically-updated list of my favorite tech products spanning pretty much all domains of use.

Here and there I add a few notes!



## My OS: Ubuntu Linux (LTS)

**Ubuntu Linux (LTS releases)**

I've been using Linux as my day to day OS for more than 15 years!

I've spent my fair share of time distro-hopping and have run Debian, Gentoo, Arch (among others) at different times.

But over time I've come to prefer a reliable LTS Ubuntu distro as the backbone of my system.

The only hard recommendation I'd make to somebody thinking of adopting Linux is to use the LTS releases. I learned this the hard way when poorly tested releases broke package managers, GPU configs, etc.

## Desktop Environment: LXDE (Still!)

**LXDE**

When I started using Linux I was a poor university student without a lot of disposable income.

LXDE allowed me to run Ubuntu on old hardware as if it were brand spanking new! Even though I finally own a desktop computer with some decent firepower in it, I've been using LXDE for so long that it's an impossible habit to break!

I played around with tiling window managers for a period (they're cool). But I think that LXDE strikes a happy medium between usability and minimalism (every time I use Windows or even Unity I'm blown away by how bloated the DEs are with graphic effects and the like)

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

## Backup and Recovery Software

I've documented a lot of my backup approach here on Github. 

But to cut to the essentials.

For backing up my Linux OS:

- **Timeshift** is a great utility for creating convenient system restore points allowing you to quickly roll back the filesystem if you (or a package) messes something up. But it's not wise to consider it a bone fide backup tool (for one, it's typically run on the same physical hardware as the machine you're protecting).

For actual backups, I personally feel most comfortable going with block-level disc imaging tools that really try to mop up every last byte of information on the disc.

The two I use frequently are: **Veeam Agent for Linux** and **Clonezilla** (both have plenty of merits.). I try to clone my OS every 3 months.

