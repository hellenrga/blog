+++
date = '2025-01-16T11:24:08-03:00'
draft = false
title = 'Increasing disk size at Virtual Box using GParted'
tags = ['VM', 'Homelab', 'Problem-solving']
+++

## I had to increase my VMbox disk size. Here's How I did It

## Step-by-step guide

1 - Go to the Virtual Media Manager of the VM you want to increase the disk size

![file-tools-vmmanager](/images/file-tools-vmmanager.png)

2 - Find the disk you want to grow and double-click it

![double-click-disk](/images/double-click-disk.png)

3 - At the end of the screen, drag the square to the right to increase its size.

![disk-size-increase](/images/disk-size-increase.png)

4 - Now, we will need to allocate this new value. If you turn on your VM and give a ``df - h `` command, you'll se the size remain the same

![terminal-command-disk-size](/images/terminal-command-disk-size.png)

5 - We'll use GParted for making this disk allocation. Download the iso [here](https://gparted.org/download.php)

![gparted-download](/images/gparted-download.png)

6 - After the download is finished, open VM VirtualBox, go to the settings of the VM you're growing, then go to storage, then go to Adds Optical Drive.

![vm-settings-storage](/images/vm-settings-storage.png)

7 - Go to Add, then select the .iso you just installed.

![selecting-gpart-iso](/images/selecting-gpart-iso.png)

8 - Select the .iso then click choose at the end of the screen

![click-choose-gparted](/images/click-choose-gparted.png)

9 - Now, initialize the VM. You now should see this screen

![gparted-initialized](/images/gparted-initialized.png)

10 - Give an Enter, know you may be seeing this. Also give an enter.

![console-data-interface](/images/console-data-interface.png)

11 - After selecting the langue, select 0 to start GParted with its graphic interface.

![select-0-gparted](/images/console-data-interface.png)


