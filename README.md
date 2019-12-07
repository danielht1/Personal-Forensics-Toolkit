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
 
- YARA
  - YARA is a tool designed to help malware researchers identify and classify malware samples by using regular expression matching. The project is open source and available to anyone who wants to use it. 
  - I used YARA in a Ubuntu image to create rules for finding regular expressions in a text document rather than working with malware signatures. The purpose was simply to learn and understand the feel of this software and then to extend that to what it would be like to work with malware. 
  - YARA documentation can be found at: https://yara.readthedocs.io/en/latest/
    - Indcluded in the documentation are all the instructions necessary to install and get started with YARA. 
   YARA did have a bit of a learning curve that took some time to grasp, but overall the software is not difficult to learn and implement. 
   
- Grep, Suricata, and tcpdump
  - These three tools are clustered together because I used them in conjunction with each other for one lab assignment. 
  - Grep processes text line by line and will print out the matching pattern that is defined by the user. Suricata is an open source threat detection engine. It is used in IDS, IPS, secutiry monitoring, and pcap processing. The latter is what I used it for. tcpdump is a command line packet analyzer. It was used with suricata for analyzing a sample pcap.
  - Suricata can be found at: https://suricata-ids.org/
  - Grep and tcpdump are often included in Linux distros

- Wireshark
  - Wireshark is a commonly used network protocol analyzer. It can be used to look at network traffic as a whole, or it can be drilled down into to see specific network behavior at the packet level. 
  - This tool was used multiple times throughout the semester to analyze various network behaviors. Most of the time it was used for analyzing previously captuted pcaps, but for one lab I did use it to capture and analyze mirrored activity across a switch.
  - Wireshark can be found at: https://www.wireshark.org/

- FTK Imager
  - Listed separately from FTK listed above. FTK Imager is an imaging tool used for data acquision for forensic evidence. This program does not analyze the drive image like the tool previously listed. 
  - FTK Imager was a very easy tool to use. It was used with a write blocker to take a bit for bit physical copy of two computer hard drives. The program even creates an case file for you as you are creating the copy.
  - FTK Imager can be found at: https://accessdata.com/product-download/ftk-imager-version-4-2-1

- Netcat
  - A computer networking utility tool used for remote data acquisition.
  - Netcat can easily be installed on a Linux distro. I used it on a Ubuntu image to acquire data from another Ubuntu VM image. 
  
- Snort
  - "An open source intrusion prevention system capable of real-time traffic analysis and packet logging." It can also be used for offline packet analysis on previously captured network traffic.
  - In class, we were able to download and install snort with the speicific configurations we were given by the professor. We only used it briefly for a short analysis of a packet capture. 
  - Snort can be found at: https://www.snort.org/
  
- Volatility
  - An open source tool for memory acquision and analysis. This program can even be used as a digital forensics framework for incident response and malware analysis in a dymamic case. 
  - Volatility is a solid command line memory analysis tool that is not difficult to use. When you need help to figure out an applicable command, the help menu gives a good description of the options that are available according to the profile/image you are running analysis against. 
  - Sometimes you have to search around for a better explanation for the information you are given by Volatility. There were multiple processes and functions I was not familiar with, so I had to learn what they were in order to determine if they were affected by malware or not.
  - Volatility can be found at: https://www.volatilityfoundation.org/  
  
- Autopsy
  - Autopsy is an open source digital forensics platform. Used for hard drive investigation, the program will ingest a drive image and perform an automatic initial analysis of the image. 
  - Autopsy was far easier to use than FTK for me. The initial analysis went through and compiled a folder of files according to their extensions so it was really easy to find a group of images I was looking for. It also created a directory of files that were of mismatched extensions so I could look directly at those and determine that they were also images I was looking for, even though they did not have image extensions. 
  - Autopsy can be found at: https://www.autopsy.com/
 
