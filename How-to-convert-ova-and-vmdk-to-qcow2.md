---
Layout: Post
Title: How to convert ova and vmdk to qcow2
Author: N̷̘̩̠͙̬̫̉͑̉͘͜ą̶͓̳͍̙̻̱̎̓̄̈́́́̈̒̀̐͘̕͝͝ṇ̸̢͉̂̽̎̾̋͛̇̉̊̚͜j̷̢̧̲̬̥̦̼͓̖̼̄̅u̸̞͎̻̍̀̋͋̊̀̓͑̈́͘͘á̴̺̫̮͈̥̳͐̍̚ṉ̴͓̯̺͎͓̅̍̌̆̚͝ N Torres
---

### Contact
- [LinkedIn](https://www.linkedin.com/in/nanjuan/)
- Email: nestor@nntorres.com

### Table
1. [Prerequisites](#preinfo)
2. [Summary](#Summary)
3. [PC Prerequisites](#First)
4. [Linux Terminal Steps](#Second)
5. [qemu-units installation](#Third)
6. [.OVA Convert Section 1](#Fourth)
7. [.vmdk Convert Section 2](#Five)

## Prerequisites <a id="preinfo"></a>
1. Have a [Virtual Machine](https://github.com/Nanjuan/Hacking-Tools-Virtualization-Tutorials/blob/master/VirtualBox_setup_with_kali.md) install


## Summary <a id="Summary"></a> 
This tutorial is for you to be able to convert ova and vmdk virtual machines to qcow2 to used it in enviroments that used qcow2 format as VMs.  


<br>

| Type of VMs | Description                                                                                                      |
|-------------|------------------------------------------------------------------------------------------------------------------|
|    VM       | Stand for Virtual Machine                                                                                        |
| name.ova    | The .ova file is one type of VM extension mainly used in Virtual Box or VMware.                                  |
| name.vmdk   | The .vmdk file is one type of VM extension mainly used in VMware and it have two extra files with it .ovf and .mf|


## PC Prerequisite <a id="First"></a>


1. Make sure that if any `disk` was mounted to the VM that is remove from the `device setting` on the `Virtual Machine` program (`Virtualbox`, `VMware`) and that the `display setting` is set to `auto` since I have seen that give problem when the resolution is set to a specific resolution. Any extra `device` that was mounted need to be `remove` too. 


- First make sure the `VM` is `power off`. 
- On `VMware` right click on the `VM` you want to `convert` and `click` on `setting`. 
- Then make sure that `CD/DVD (IDE)` is set to `Auto detect`.
- Then make sure that `Display` is set to `Auto detect` as well. 

![Section1](/assets/qcow2-1.png)

- On `Virtualbox` go to `setting` on the `top left area of the program`.
- Then go to `storage` and make sure is `empty` like the picture bellow. 
- Here as long as you `did not change` the `display setting` that should be ok if you did set to `default` again.

![Section1](/assets/qcow2-2.PNG)



## Start the Conversion on a linux (Ubuntu,Kali,Other) Terminal <a id="Second"></a>

2. First step is to export the machine you want to convert to either 
<br>

| VM Formats to conversts |
|:-----------------------:|
|        vm.ova           |
|        vm.vmdk          |

- Make sure that the VM file you want to converts is on the a Linux machine that have qemu.utils install to make it easier to convert the vm. 


## Make sure qemu-utils are install <a id="Third"></a>

3. To make sure you have qemu-img install.

- open terminal 
- type `qemu-img` and press `enter`  
- you should get sometime alone the line of `qemu-img: not enought arguments` this will let you know that qemu-utils are install on your linux computer
- otherwise on the same `terminal` run `sudo apt-get update` after that is done run `sudo apt-get install qemu-utils` 
- Next step is to `navigates` to the `folder` that have the `VM you exported` and want to `convert`. 
- if you have `vm.ova` follow `section 1` `otherwise` go to `section 2`


## Section 1 <a id="Fourth"></a>

5. Here is how to `extract` a `.ova` to `.vmdk` so you can continue on `section 2`

- After navigating to the folder run `tar -xvf inputVM.ova` the `VM.ova` would be the name of your vm that you want to covert so that might vary for you VM. 
- This might take a `while` to `decompress` depending on the `side` of the `vm`. 
- This will give you the `.ovf` `.mf` `.vmdk` that you need to convert now you can move to `section 2`

![Section4](/assets/qcow2-3.PNG)

![Section4](/assets/qcow2-4.PNG)

## Section 2 <a id="Five"></a>

6. Here is the step to convert .vmdk to .qcow2

- First step when you have the `VM.vmdk`  is to run the `qemu-img` command to convert from `.vmdk` to `.qcom2`
- Open terminal and `navigate to the folder` that have the `VM.vmdk` you want to `convert`. 

![Section5](/assets/qcow2-5.PNG)

- Then run the command `qemu-img convert -O qcow2 inputVM.vmdk outputVM.qcow2`. 
- This `will take some time depending on the size of the VM` and `computer processing power`. 

![Section5](/assets/qcow2-6.PNG)

![Section5](/assets/qcow2-7.PNG)

# And your done!!!

## Now you can import this new VM.qcow2 to any KVM Hypervisor like Antsle box and the VM will be read and write and not only read. 

## Well your done!!!! any question email me!!!!! Any feedback email me!!!! Any spelling error sorry and email me!!!! Thanks!!!!!