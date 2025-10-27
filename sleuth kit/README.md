
# Experiment 06: Use Sleuth Kit to Analyze Digital Evidence

## Aim
To use **The Sleuth Kit (TSK)** command-line tools to analyze a disk image and recover digital evidence.

---

## Description
The **Sleuth Kit (TSK)** is an open-source suite of command-line tools used for digital forensics. It allows forensic investigators to examine disk images, analyze file systems, list files and partitions, recover deleted data, and extract file metadata. Optional timeline analysis helps track file activity over time. All findings can be compiled into a report for documentation and secure storage.

---

## Procedure

### Step 1: Install Sleuth Kit
**Download Sleuth Kit:**
- Visit the official Sleuth Kit website or [Google Drive link](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v).
- Download the latest version for Windows.

**Install Sleuth Kit:**
- Run the installer and follow the on-screen instructions to complete installation on your Windows machine.

---

### Step 2: Acquire the Disk Image
Before analysis, a disk image of the evidence source is required. This image can be from a hard drive, memory card, or any other storage device.

**Create Disk Image:**
- Use tools like **FTK Imager** or **dd** to create a bit-by-bit copy of the storage device.
- Ensure the image format is compatible with Sleuth Kit — `.dd`, `.raw`, `.img`, or `.E01`.

**Download Required Files:**
- `4Dell Latitude CPi.E01`
- `4Dell Latitude CPi.E02`

These sample files can be downloaded from the Google Drive link.

---

### Step 3: Mount the Disk Image (Optional)
Mounting the disk image makes it easier to browse and analyze the file system.

**Mount the Image:**
- Use **OSFMount** to mount the image as a virtual drive on your Windows system.  
- This step is optional but simplifies navigation within the file system.

---

### Step 4: Analyze the File System
Use Sleuth Kit commands from the command prompt to analyze the image and locate evidence.

**Navigate to the Sleuth Kit Directory:**
- Open **Command Prompt**.
- Navigate to the directory where Sleuth Kit is installed.

**Identify File System Type with `fsstat`:**
```bash
fsstat "4Dell Latitude CPi.E01" > filesystem_info.txt

