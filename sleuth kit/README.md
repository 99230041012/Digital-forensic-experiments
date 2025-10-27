
# Experiment 06: Use Sleuth Kit to Analyze Digital Evidence
## Aim
To use **The Sleuth Kit (TSK)** command-line tools to analyze a disk image and recover digital evidence.

---

## Description
The **Sleuth Kit (TSK)** is an open-source suite of command-line tools used for digital forensics. It allows forensic investigators to examine disk images, analyze file systems, list files and partitions, recover deleted data, and extract file metadata. Optional timeline analysis helps track file activity over time. All findings can be compiled into a report for documentation and secure storage.


<img width="1474" height="701" alt="Image" src="https://github.com/user-attachments/assets/21914a95-ceb8-4206-ab95-5d60e01cda07" />
## Procedure

### Step 1: Install Sleuth Kit
**Download Sleuth Kit:**
- Visit the official Sleuth Kit website or [Google Drive link](https://drive.google.com/drive/u/1/folders/1ilSFY7Tqn2L7AjQGhq8yJ8kixc_xTU-v).
- Download the latest version for Windows.

**Install Sleuth Kit:**
- Run the installer and follow the on-screen instructions to complete installation on your Windows machine.
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/9b29bdb4-d5ac-4d36-9705-5b0b92af77bc" />
---
<img width="703" height="449" alt="Image" src="https://github.com/user-attachments/assets/fc4598d6-29ad-4bd7-bc47-fe284dbaaadb" />
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

<img width="698" height="230" alt="Image" src="https://github.com/user-attachments/assets/cc666edc-0744-423d-8854-115310456cee" />
**Navigate to the Sleuth Kit Directory:**
- Open **Command Prompt**.
- Navigate to the directory where Sleuth Kit is installed.
<img width="703" height="449" alt="Image" src="https://github.com/user-attachments/assets/fc4598d6-29ad-4bd7-bc47-fe284dbaaadb" />
**Identify File System Type with `fsstat`:**
```bash
fsstat "4Dell Latitude CPi.E01" > filesystem_info.txt


<img width="698" height="230" alt="Image" src="https://github.com/user-attachments/assets/cc666edc-0744-423d-8854-115310456cee" />



<img width="698" height="230" alt="Image" src="https://github.com/user-attachments/assets/cc666edc-0744-423d-8854-115310456cee" />
<img width="701" height="467" alt="Image" src="https://github.com/user-attachments/assets/667906a3-eab9-4312-90b8-61c6790e26ee" />
<img width="745" height="295" alt="Image" src="https://github.com/user-attachments/assets/54d52ec3-126f-4e54-9e5c-76ec76f7a5cd" />
<img width="1011" height="483" alt="Image" src="https://github.com/user-attachments/assets/9c772b76-161f-4184-abc7-d6c483b9aa09" />
<img width="959" height="486" alt="Image" src="https://github.com/user-attachments/assets/f1848b26-82c4-49dc-a210-63b023c0316b" />
<img width="950" height="713" alt="Image" src="https://github.com/user-attachments/assets/5486f419-ed53-4da1-a7d7-fd16cd993273" />
<img width="930" height="466" alt="Image" src="https://github.com/user-attachments/assets/9b06b3ab-c8f1-4a22-bd65-3e39ea6d765b" />
<img width="1477" height="658" alt="Image" src="https://github.com/user-attachments/assets/9bd593e9-09b5-4077-a943-ef58c51b300a" />
<img width="1474" height="701" alt="Image" src="https://github.com/user-attachments/assets/21914a95-ceb8-4206-ab95-5d60e01cda07" />
