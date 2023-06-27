![il_fullxfull 4618057718_hux2](https://github.com/Myrkridia/Notes-101/assets/88998826/47539fd1-fe62-42eb-82be-6a4228322cc2)

# FINE

This method is what I used for after turnng an old mac book (2011) into a Kali Linux machine via partitioning and installing the needed firmware for the Linux machine to use wifi.

#

**Cool notes**

If you use Parrot Sec, this repo is not needed. It works fine.

#

**Things you will need**

The mac book and a USB drive.

#

**Download**

Once you have installed Kali Linux via partitioning, restart and boot back into MacOS.

You will need to download 2 files.

1. `b43 firmware fwfinger`

http://www.lwfinger.com/b43-firmware/

and choose from the list; I selected and used

`broadcom-wl-6.30.163.46.tar.bz2` 

Download: `broadcom-wl-6.30.163.46.tar.bz2`

2. `b43 fw-cutter`

https://packages.debian.org/bookworm/b43-fwcutter

You will want to choose your architecture; for these older machines, AMD64 works.

Select

`b43-fwcutter_019-8_amd64.deb`

And choose a server closest to your region.

Download: `b43-fwcutter_019-8_amd64.deb`

#

**USB drive**

Once both files are downloaded, you will want load them onto your USB drive. BUT make sure it is formatted for the Linux machine to recognize it.
If you have problems, reformat the USB drive using **DiskUtility** to make the format into MS-DOS.

#

**Extraction**


Once that's done, restart and boot into Kali Linux.

Plug the flashdrive and drop the files onto your desktop.

Use your terminal and `cd` to `~/Desktop`

You will be extracting the two files.

Run command:

`sudo dpkg -i b43-fwcutter_019-8_amd64.deb`

Next run command:

`tar xfvj broadcom-wl-6.30.163.46.tar.bz2` 

#

**Installation**

Run command:

`sudo b43-fwcutter -w /lib/firmware broadcom-wl-6.30.163.46.wl_apsta.o`

#

**At last**

That should do it.

Restart your machine and boot in Kali Linux.

Check to see if the internet/wifi icon in the interface have appeared in the drop down menu.

Connect and see if you have acquired internet connection.







