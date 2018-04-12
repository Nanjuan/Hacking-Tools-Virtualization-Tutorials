---
Layout: Post
Title: VirtualBox & kali setup
Author: N̷̘̩̠͙̬̫̉͑̉͘͜ą̶͓̳͍̙̻̱̎̓̄̈́́́̈̒̀̐͘̕͝͝ṇ̸̢͉̂̽̎̾̋͛̇̉̊̚͜j̷̢̧̲̬̥̦̼͓̖̼̄̅u̸̞͎̻̍̀̋͋̊̀̓͑̈́͘͘á̴̺̫̮͈̥̳͐̍̚ṉ̴͓̯̺͎͓̅̍̌̆̚͝ N Torres
---

### Contact
- [LinkedIn](https://www.linkedin.com/in/nanjuan/)
- Email: nestor@nntorres.com

### Table
1. [Prerequisites](#preinfo)
2. [Summary](#Summary)
3. [PC Prerequisites](#First)
4. [VirtualBox installation](#Second)
5. [Kali Virtual Machine](#Third)
6. [Network adapter setup](#Fourth)

## Prerequisites <a id="preinfo"></a>
1. Have [VirtualBox](https://www.virtualbox.org/wiki/Downloads) Downloaded
2. Have [Kali pre-build OS for VirtualBox](https://www.offensive-security.com/kali-linux-vm-vmware-virtualbox-hyperv-image-download/) Downloaded
3. Have [VirtualBox Extension pack](https://www.virtualbox.org/wiki/Downloads) Downloaded
4. Enable Virtualization on bios

## Summary <a id="Summary"></a> 
This tutorial is for you to be able to install and setup VirtualBox on a Windows computer and with minimal changes on Mac OS and change network adapter. 


<br>

| Network adapters | Description                                                                      |
|------------------|----------------------------------------------------------------------------------|
| NAT              | NAT gateways sit between two networks adn emulated by your computer              |
| Bridge Network   | Bridge is exacly that when you give direct access to the computer network adapter|


## PC Prerequisite <a id="First"></a>


1. Go to `Taskbar` and right click and then select `Task Manager`

- After selecting `Task Manager` select `Performance`
- This will let you know if your computer have `Virtualization`
- Look at the bottom left for `Virtualization` to see if is `Enabled` or `Disable`
- If `Virtualization` is `disable` go to google and search for your pc manufacture on how to enable `Virtualization`.
- You will get a error like the one bellow if your `virtualization` is `disable` and you try to install `VirtualBox`. 

![Section1](/assets/2-1.png)

![Section1](/assets/1.png) 
![Section1](/assets/2.png)


## Start the VirtualBox installation <a id="Second"></a>

2. Go to where you download your files to install `VirtualBox`.

- Double click on the `VirtualBox` installation file.

![Section2](/assets/3.png)

- Then go through the installation process. 

![Section2](/assets/4.png)

![Section2](/assets/5.png)

- When your done you will be welcome with similars screens. 

![Section2](/assets/6.png)

![Section2](/assets/7.png)

## Start the Instalation of Kali Virtual Machine <a id="Third"></a>

3. Go back to the folder where your downloaded files are located. 

- Double click on the `kali***.ova` file to import the virtual machine this might take couple of second to show the pop up then click `import` and wait.  

![Section3](/assets/8.png)

- After the import is done double click on the `Kali` virtual machine to start machine if you get a error like bellow you must install `VirtualBox Extension Pack`

![Section3](/assets/9.png)

- Go to where you have your downloaded the install files and `double click` on `VirtualBox Extension Pack` if `VirtualBox` is open check the pop up or a second windows that might been open and click `Install`, and go throught the installation process. 

![Section3](/assets/10.png)

![Section3](/assets/11.png)

4. Last step start your `Kali Virtual machine` again. 

- The log in information for the Kali pre build machine is
- `Username:` `root`
  `Password:` `toor`

![Section3](/assets/11.png)

- And!!!!!!!!!!! your done with the basic install of Kali on VirtualBox. 

![Section3](/assets/12.png)

## Network adapter setup <a id="Fourth"></a>

5. The fun part deciding to used `NAT` or `Bridge` network.
- If you want to have your network router throught your computer leave `NAT`
- If you want to have your virtual machine connected directly to the network card and get a external ip set it up to `Bridge` mode. 

6. First select `Machine` on the top left to get the drop down.

 ![Section3](/assets/13.png)

- Then select `Settings` to open the setting windows. 

![Section3](/assets/14.png)

- The select `Network` to get to the network settings. 

![Section3](/assets/15.png)

- Then select on the second drop down your `Wi-Fi` or `External Wi-Fi device` and press ok. 

![Section3](/assets/16.png)


## Well your done!!!! any question email me!!!!! Any feedback email me!!!! Any spelling error sorry and email me!!!! Thanks!!!!!