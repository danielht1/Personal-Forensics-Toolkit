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
  - SANS Investigate Forensic Toolkit, based on the Ubuntu 14.04

TOOLS/HARDWARE

- Tableau eSATA Forensic Bridge physical write blocker
  - Allows for a connection to be made between the digital evidence drive and the forensic workstation without allowing the workstation to write to the evidence. This maintains the integrity of the evidence.
  - The write blocker was simple and intuitive to use. I used it for one lab in this class and deemed that it was a useful tool for integrity maintenance. It was not difficult to figure out how to connect the evidence drive and the forensic workstation.

SOFTWARE

- FTK: Forensic Tool Kit
  - A full service digital forensic toolkit application that can be used for a varitey of forensics activities. 
  - FTK was a little more challenging to use for me than Autopsy, a similar program, because of the way it organized the file structure of the drive I was working on. To expand on that, I was given a .dd drive image to analyze with FTK, looking for specific images. Once FTK imported the image and did the initial analysis, I felt like I had to dig more for the information I was looking for when compared to another program. 
  - This program is not open source, but can be found at: https://accessdata.com/product-download/forensic-tools-7-2
  
 
