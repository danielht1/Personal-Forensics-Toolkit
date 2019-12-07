# Personal-Forensics-Toolkit

Tools and guides learned about and used during the course of a Digital Forensics class.

LINUX DISTRIBUTIONS

- Deft 8.2: Digital Evidence and Forensic Toolkit (DEFT)
  - A toolkit based on the Linux GNU platform. This platform can be booted from a USB stick and contains digital forensics tools that can be used for digital acquisition and analysis without running automated mounting scripts.
  - I did not personally use this tool. It was a suggested tool learned about in the course textbook: Digital Forensics and Incident Response by Gerard Johansen.
  
- Paladin
  - A Linux distribution based on the Ubuntu OS. Paladin has built in digital forensics tools for malware analysis, hashing, and imaging. It also includes a number of tools and packages thta can be used on a wide range of operating systems. 
  - I did not personally use this tool. It was a suggested tool learned about in the course textbook: Digital Forensics and Incident Response by Gerard Johansen.
  
- SANS SIFT
  - SANS Investigate Forensic Toolkit, based on the Ubuntu 14.04 platform. This system has built in tools like previously mentioned images. Included tools can be used for imaging, memory analysis, timeline creation, and other forensics tasks. This is a standalone virtual machine that is provided for free by SANS.
  - The tool can be found at: https://digital-forensics.sans.org/community/downloads.
  - I did not personally use this tool. It was a suggested tool learned about in the course textbook: Digital Forensics and Incident Response by Gerard Johansen.
  
- CAINE
  - Computer Aided Investigative Environment. CAINE is a Linux GNU distrubition for forensic purposes. This distro contians similar tools to the other distros for the same digital forensics tasks. 
  - I did not personally use this tool. It was a suggested tool learned about in the course textbook: Digital Forensics and Incident Response by Gerard Johansen.
  
- REMNUX
  - Based on Ubuntu Linux, REMNUX is a tool that focus on malware reverse engineering tools. It includes some tools that are specifically designed for analyzing Windows and Linux malware, suspicious documents, and the ability to intercept potentially malicious network traffic. 
  - I did not personally use this tool. It was a suggested tool learned about in the course textbook: Digital Forensics and Incident Response by Gerard Johansen.

TOOLS/HARDWARE

- Tableau eSATA Forensic Bridge physical write blocker
  - Allows for a connection to be made between the digital evidence drive and the forensic workstation without allowing the workstation to write to the evidence. This maintains the integrity of the evidence.
  - The write blocker was simple and intuitive to use. I used it for one lab in this class and deemed that it was a useful tool for integrity maintenance. It was not difficult to figure out how to connect the evidence drive and the forensic workstation.

SOFTWARE

- FTK: Forensic Tool Kit
  - A full service digital forensic toolkit application that can be used for a varitey of forensics activities. 
  - FTK was a little more challenging to use for me than Autopsy, a similar program, because of the way it organized the file structure of the drive I was working on. To expand on that, I was given a .dd drive image to analyze with FTK, looking for specific images. Once FTK imported the image and did the initial analysis, I felt like I had to dig more for the information I was looking for when compared to another program. 
  - This program is not open source, but can be found at: https://accessdata.com/product-download/forensic-tools-7-2
  
- OSXPMem
  - Part of the pmem suite created by the developers of Rekall. This tool is used to perform a memory capture and analysis on OSX for Mac.
   - There are some permission quirks sometimes with OSXPMem. In preparation for using this tool I read guides that explained what problems could happen and how to solve them.
   - Note: When you run the program as sudo or root you may receive the following error: $ sudo osxpmem.app/osxpmem -o Memory_Captures/mem.aff4 Imaging memory E1229 15:17:26.335978 3375588288 aff4_file.cc:289] Can not open file /dev/pmem :No such file or directory /Users/jp/Projects/osxpmem.app/MacPmem.kext failed to load - (libkern/kext) authentication failure (file ownership/permissions); check the system/kernel logs for errors or try kextutil(8). E1229 15:17:26.606639 3375588288 osxpmem.cc:283] Unable to load driver at /Users/jp/Projects/osxpmem.app/MacPmem.kext E1229 15:17:26.606714 3375588288 pmem_imager.cc:328] Imaging failed with error: -8  
To solve:  
Use the kextutil’s test parameter -t for more information. If it reveals the message "File owner/permissions are incorrect (must be root:wheel, nonwritable by group/other):”, change the permissions by running: $ sudo chown -R root:wheel osxpmem.app/. 
   - OSXPMem can be found at: http://releases.rekall-forensic.com/
  
 
