#  This is a quick tutorial on how to setup full screen on your virtual box when using Kali.
### (This *might* work on other linux distros as well but I've only tested this on Kali Linux.)

## Step One 

### Make sure you have VirtualBox AND the Extension packs installed which you can get from 
- [https://www.virtualbox.org/wiki/Downloads](https://www.virtualbox.org/wiki/Downloads)

## Step Two 

### Make sure you have Kali fully install and running.

## Step Three 

### Your Kali machine should look like this on full screen. 

![Imgur](https://i.imgur.com/kxStoxI.png)

![Imgur](https://i.imgur.com/mpjvCwF.png)

## Step Four

### On the top setting bar of the Kali vm go to devices and press (Insert Guest Additional CD image) you should see a message like below.

![Imgur](https://i.imgur.com/ImpKx5g.png)

### Then press run. You should see a error message saying Oops! ect that's normal. Press ok and move to next step. 

## Step Five

### Right-click on the cd and click where it says (Open in Terminal) like below.

![Imgur](https://i.imgur.com/s2BabYL.png)

### The window that opens should look like this. 

![Imgur](https://i.imgur.com/oNnuQTT.png)

## Step Six 

### Run the following line of code: 
> sh ./VBoxLinuxAdditions.run

### You should see a message like below. Make *sure* it says "currently not setup to build kernel module". 

![Imgur](https://i.imgur.com/Kxf2TOe.png)

## Step Seven

### Run the following line of code:
> apt-cache search linux-headers

### You are trying to find a line that looks like this line on the top of the list. Your specific version may be different than what I am showing here, depending on the *version* of Kali you have installed. The important thing is that the linux-header version number *matches* the version number of the Kali you have installed on the VM.
> linux-headers-4.14.0-Kali3-amd

![Imgur](https://i.imgur.com/Vt05KYN.png)

### Then copy that line you find that matches. You are going to use it to install the package. 

### Then run the following line of code: 
> apt-get install linux-headers-4.14.0-Kali3-amd

![Imgur](https://i.imgur.com/WNUYzpv.png)

### Press Y if it asks you to install then wait for it to be done. It should look similar to this when it is done installing that file

![Imgur](https://i.imgur.com/WbFjwWQ.png)

## Step Eight

### Run the following line of code:
> apt-cache search linux-image

### Then look for the file name like below. The version number may change. Make sure it matches with the one below.
>linux-image-4.14.0-Kali3-amd64

![Imgur](https://i.imgur.com/1wcLnTr.png)

### Then run the following line of code: 
> apt-get install linux-image-4.14.0-Kali3-amd64

### Press Y if it asks you to install. Then wait, this part can take a while to complete. It should look similar to this when it is done installing that header file. 

![Imgur](https://i.imgur.com/XME0utg.png)

## Final Step 

### Run the following line of code:
> reboot 

### Next time the computer reboots you should see the VM going into full screen when you make it full screen and use the correct resolution like below. My computer's native resolution is (1440 x 900) yours may be different.

![Imgur](https://i.imgur.com/cWM3eOk.png)

## You're done! If you have any problems please email me at or ask me in class. 
- Email: Nestor@nntorres.com
