+++
date = '2025-01-16T11:24:08-03:00'
draft = false
title = 'Increasing Disk Size in VirtualBox Using GParted'
tags = ['VM', 'Homelab', 'Problem-solving']
+++

In this guide, I’ll walk you through the process of increasing the disk size of a VirtualBox virtual machine (VM) and allocating the additional space using GParted.

---

## Step-by-Step Guide

### 1. Access the Virtual Media Manager
Go to the **Virtual Media Manager** of the VM you want to resize. You can find this under **File > Virtual Media Manager**.

![file-tools-vmmanager](/images/file-tools-vmmanager.png)

---

### 2. Select the Disk to Resize
Find the disk you want to increase in size and double-click it.

![double-click-disk](/images/double-click-disk.png)

---

### 3. Increase Disk Size
At the bottom of the screen, drag the slider to the right to increase the disk size to your desired value.

![disk-size-increase](/images/disk-size-increase.png)

---

### 4. Verify Disk Size in the VM
Start your VM and run the following command in the terminal to check the disk size: 

```bash
df -h
```

You’ll notice that the size remains the same because the additional space hasn’t been allocated yet.

![terminal-command-disk-size](/images/terminal-command-disk-size.png)

---

### 5. Download GParted ISO
We’ll use **GParted** to allocate the new disk space. Download the ISO file [here](https://gparted.org/download.php).

![gparted-download](/images/gparted-download.png)

---

### 6. Attach the GParted ISO
1. In VirtualBox, go to the **Settings** of the VM you want to resize.
2. Navigate to **Storage**.
3. Click on **Add Optical Drive**.

![vm-settings-storage](/images/vm-settings-storage.png)

---

### 7. Select the GParted ISO
1. Click **Add** and locate the GParted `.iso` file you just downloaded.
2. Select the ISO, then click **Choose** at the bottom of the screen.

![selecting-gpart-iso](/images/selecting-gpart-iso.png)
![click-choose-gparted](/images/click-choose-gparted.png)

---

### 8. Boot the VM with GParted
Start the VM. You should see the following screen:

![gparted-initialized](/images/gparted-initialized.png)

Press `Enter`.

---

### 9. Launch GParted
When prompted, press `Enter` again to proceed with the default options. 

![console-data-interface](/images/console-data-interface.png)

After selecting your language, choose option `0` to start GParted with its graphical interface.

---

### 10. GParted Interface
Once GParted loads, you’ll see its graphical interface:

![gparted-interface](/images/gparted-interface.png)

---

### 11. Resize the Partition
1. Double-click the partition you want to resize.
2. Drag the slider to allocate the remaining unallocated space.
3. Click **Resize/Move**.

![resize-vm](/images/resize-vm.png)

---

### 12. Apply the Changes
Click **Apply All Operations** to finalize the resizing.

![apply-operation](/images/apply-operation.png)

---

### 13. Detach the GParted ISO
1. Shut down the VM.
2. Go to **Settings > Storage**.
3. Remove the GParted ISO from the **Optical Drive**.

![remove-attachment-gpart](/images/remove-attachment-gpart.png)

---

### 14. Verify the New Disk Size
Start your VM again. Run the following command to check the new disk size:

```bash
df -h
```

You should now see the updated disk size.

![new-disk-size](/images/new-disk-size.png)

---

## Conclusion

Congratulations! 🎉 You have successfully increased the disk size of your VirtualBox VM and allocated the additional space using GParted.