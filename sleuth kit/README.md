Ex No - 06: Use Sleuth Kit to Analyze Digital Evidence
Description
The Sleuth Kit (TSK) is a collection of command-line tools that allow you to analyze disk images and recover digital evidence. This document provides a step-by-step guide to using Sleuth Kit on a Windows machine to analyze digital evidence.

Step 1: Install Sleuth Kit
Download Sleuth Kit:
Visit the official Sleuth Kit website or Google Drive link

Download the latest version for Windows

Install Sleuth Kit:
Run the installer and follow the instructions to install Sleuth Kit on your Windows machine

Step 2: Acquire the Disk Image
Before analysis, you need a disk image of the evidence. This can be an image of a hard drive, memory card, or any other storage device.

Create Disk Image:
Use a tool like FTK Imager or dd to create a bit-by-bit copy of the storage device

Ensure the image is in a format supported by Sleuth Kit, such as .dd, .raw, .img, or .E01

Download the required files from Google Drive:
4Dell Latitude CPi.E01

4Dell Latitude CPi.E02

Step 3: Mount the Disk Image (Optional)
Mounting the disk image makes it easier to analyze the file system.

Mount the Image:
Use a tool like OSFMount to mount the image as a virtual drive on your Windows system

This step is optional but helps with navigating the file system easily

Step 4: Analyze the File System
Use Sleuth Kit tools to analyze the file system and locate evidence.

Navigate to the Sleuth Kit Directory:
Open Command Prompt and navigate to the directory where Sleuth Kit is installed

Identify File System Type with fsstat:
bash
fsstat "4Dell Latitude CPi.E01" > filesystem_info.txt
This command outputs information about the file system, which is crucial for understanding the structure of the disk.

List Partitions with mmls:
bash
mmls "4Dell Latitude CPi.E01" > partitions.txt
This command lists the partitions within the image file.

Analyze File System with fls:
bash
fls -r "4Dell Latitude CPi.E01" > file_list.txt
This command recursively lists files and directories in the file system, showing their metadata.

Recover Deleted Files with icat:
bash
icat "4Dell Latitude CPi.E01" [inode number] > [output file]
Replace [inode number] with the inode of the file you want to recover, which you can find from the fls output.

Step 5: Analyze Metadata
Extract metadata from files to understand more about the file's history.

View Metadata with istat:
bash
istat "4Dell Latitude CPi.E01" [inode number] > metadata_info.txt
This provides detailed information about a file, including timestamps, size, and allocation status.

Step 6: Timeline Analysis (Optional)
Creating a timeline of file activity can be crucial in an investigation.

Create Timeline with mactime:
Generate a body file using fls:

bash
fls -m / -r "4Dell Latitude CPi.E01" > body.txt
Then create the timeline:

bash
mactime -b body.txt > timeline.txt
The timeline includes MAC (Modified, Accessed, Changed) times of files.

Step 7: Generate a Report
Document your findings by compiling all the data into a comprehensive report.

Compile the Data:
Gather all the output files:

filesystem_info.txt

partitions.txt

file_list.txt

metadata_info.txt

timeline.txt

Analyze and Document:
Review the findings, highlight important evidence

Write a report summarizing the investigation's results

Step 8: Finalize and Store Evidence
Ensure that all evidence and reports are securely stored.

Archive Evidence:
Use a secure method to archive the disk image and analysis results

Ensure integrity and confidentiality

Store Securely:
Store the archived data in a secure location

Follow the chain of custody procedures

Result:
By following these steps, you can use Sleuth Kit on a Windows machine to effectively analyze digital evidence and extract crucial information for your investigation.

Expected Output Files:
filesystem_info.txt - File system type and details

partitions.txt - Partition table information

file_list.txt - Complete directory listing

metadata_info.txt - File metadata information

timeline.txt - File activity timeline

Recovered files from icat commands
