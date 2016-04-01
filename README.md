# Midterminators Control System

This repo is for controlling the unicorn-drive robot that the Midterminators built for the Jerry Sanders Design Competition from 2012-2014.  The software runs on an National Instruments sbRIO (see Documentation folder), powered by LabVIEW.  To view or edit this code, you will need LabVIEW.



## Getting Started with LabVIEW

To install LabVIEW on your computer, first you need to acquire a UIUC LabVIEW license, and then you need to download and install LabVIEW.

You can download a free LabVIEW license from UIUC's Webstore (https://www.google.com/url?q=https%3A%2F%2Fwebstore.illinois.edu%2FShop%2Fproduct.aspx%3Fzpid%3D1254&sa=D&sntz=1&usg=AFrqEzeMkyqJyJNuWTLUyoGYq59NdqQcwg).  "Purchase" the software license for free, and your serial number will be listed below under "Additional Instructions."  You do not need to download LabVIEW from the Webstore here.

Once you have a serial number, you need to download and install LabVIEW along with the supporting modules.  LabVIEW can be downloaded for free from National Instruments' website (https://www.google.com/url?q=https%3A%2F%2Flumen.ni.com%2Fnicif%2Fus%2Fevaltlktembdes%2Fcontent.xhtml&sa=D&sntz=1&usg=AFrqEzfaorI72uen_7QvFI-SPZ2PPevw-g).  Install all the packages under step 1 except the NI LabVIEW Compile Cloud Service Free Trial.  Even if you have a 64-bit computer, you should install the 32-bit version because the necessary modules are only supported on 32-bit.  The packages may all be downloaded in parallel.  Once the downloads are all finished, you will need to first install LabVIEW, then the NI-RIO Driver, then the rest of the other three packages.  Use the serial number from the UIUC Webstore when installing each product.  When asked to register your product, select "register later" and continue with the trial version.  When you are done installing all the packages, open the NI MAX (Measurement and Automation Explorer) program.  NI MAX displays all the connected systems, and all the installed software on each one.  Ensure that you have LabVIEW, LabVIEW Real-Time Module, LabVIEW FPGA Module, FPGA Compilation Tools, and the NI-RIO Drivers installed on your local machine.

Last, you need to tell LabVIEW to look remotely for a software license when it boots up.  To do this, go to Programs and launch the NI License Manager (Start->Programs->National Instruments).  Open the Options menu and select Preferences.  Enter the license server: ni.webstore.illinois.edu:27001.

At this point, you should be all set!  Just remember, you need to be connected to a UIUC network or connect via VPN before you boot up LabVIEW so that a remote license can be properly acquired.



## Connecting to the sbRIO

Connect the sbRIO to the same subnet as your computer. Turn on DIP switch 3 (factory reset), power on the sbRIO, wait twenty seconds, and turn off the DIP switch. The sbRIO should show up under NI MAX with IP address 0.0.0.0. Set a static IP address within the valid range allowed by your router/subnet, as it will be easier to find the sbRIO when it is networked to a VI later on.  Save all settings.  Also, go ahead and give it a unique name, saving settings again.



## Using Git with LabVIEW

Git is a VCS (Version Control Software) used to keep track of changes to code. It is needed to access the code source files which are hosted on a remote server, download them to your local machine, and uploading/merging any edits you make to the code.  You can learn more about Git and how to install it by going to our Git page.

Since LabVIEW's files are all graphical and proprietary in nature, you need to use LabVIEW's tools to difference or merge conflicting versions of files during a push or pull operation. To do this, follow the instructions at https://docs.google.com/document/d/1Lmx9WI1g_ObB03Vrlfb7QU3ochz1q_YRGM8dPi0R8g8/edit to tell Git to use LabVIEW's diff tools.

Other than that, Git can be used to perform all the normal operations as with anything else.  Make sure to set up a repository for your team under our Bitbucket account, and get coding!



## IMPORTANT NOTES:

Currently, the FPGA compiler is not supported on Windows 8.  Windows will still let you install the FPGA Compile Farm, but when you try to compile the FPGA, it will say that it cannot find the compilation tools.
