# WSL
Video Walkthrough - https://www.youtube.com/watch?v=4yLeHlA2ia8

NOTE!!!  This build is for advanced users only because a Windows Insider Preview build has to be used. I tried for weeks to get it working on a General Availability image and it is not supported, so this build must be used. I take no responsibility for corrupted or lost data. Use at your own risk! 
# Instructions
	You MUST be using Windows 10 Insider Preview Dev channel Build 21354.1 ( https://drive.google.com/file/d/1rKIihZ2EgC8_DfVlWRHsg6OMdHt-fDjl/view?usp=sharing) 
	AND
	Windows Subsystem for Linux Update 5.4.72 ( https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) 

	1) Download the Windows 10 Dev Channel Build 21354 https://drive.google.com/file/d/1rKIihZ2EgC8_DfVlWRHsg6OMdHt-fDjl/view?usp=sharing
	2) Install as normal. Recommend a VM, but can be installed on a physical machine. 
	3) Make sure all virtualization features are turned on for your environment.
	4) Download and install the Windows Subsystem for Linux Update 5.4.72 (https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)
	5) Reboot the machine
	6) Open Powershell as Administrator and type the following:  wsl --set-default-version 2
	7) Open the Windows Store and search for Ubuntu 20.04. Download and install. 
	8) Launch when installation is complete. You should see a $ prompt
	9) Enter uname -a to verify the kernel. Should report 5.4.72-microsoft-standard-WSL2
	10) Enter sudo apt update && sudo apt full-upgrade && sudo apt install cpu-checker && sudo apt install acl
	11) Enter sudo kvm-ok
		a. You should see the following:      INFO: /dev/kvm exists. KVM acceleration can be used.
	12)  If you get a message that /dev/kvm does not exist, or if you get an access denied to KVM, enter the following commands:
		a.  curl -o setup-kvm.sh https://join.golem.network/setup-kvm.sh 
		b.  sudo chmod +x ./setup-kvm.sh 
		c.  ./setup-kvm.sh
	13) Run the Golem Provider installation script to setup your Golem Provider.
