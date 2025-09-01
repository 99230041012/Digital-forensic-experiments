# Experiment 01: Evidence Acquisition Using AccessData FTK Imager

## Objective
To acquire and analyze forensic evidence (volatile and non-volatile memory) using FTK Imager.

## Tools Used
- FTK Imager (Portable / Installed)
- USB Pen Drive / HDD (for portable version)
- Write Blocker (to prevent evidence modification)

## Procedure

### Acquiring Volatile Memory
1. Open **FTK Imager** → Click on **Capture Memory**.
2. Options available:
   - **Include Pagefile (pagefile.sys):** Stores extra volatile data when RAM is full.
   - **Include AD1 file:** Creates an FTK image file for later use.
3. Click **Capture Memory** to start acquisition.
4. Once complete, a `.mem` file will be generated in the chosen destination folder.

📌 **Note:** Pagefile often contains valuable evidence. Always enable this option.

---

### Acquiring Non-Volatile Memory (Disk Image)
1. Open **FTK Imager** → Select **Create Disk Image**.
2. Choose the source:
   - Physical Drives (entire hard disk)
   - Logical Drives (partitions)
   - Image Files
   - Folders / CDs / DVDs
3. Connect the source disk via **Write Blocker** to maintain integrity.
4. Choose the required image format:
   - **Raw (dd):** Simple, tool-independent format.
   - **SMART:** Linux-oriented, compressed format.
   - **E01:** Proprietary EnCase format with metadata, MD5 hash, and compression.
   - **AFF / AFF4:** Open forensic format with advanced features.
5. Enter **Case Details** (Examiner name, notes, case ID, etc.).
6. Set **Image Destination**:
   - File name
   - Fragment size (set to `0` for a single file).
7. Enable **Verify Image After Creation** for hash validation.
8. Click **Start** → Acquisition begins.

📌 **Note:** Larger images will take longer if verification is enabled, but this step is crucial for maintaining evidence integrity.

---

## Result
- Successfully captured volatile memory (`.mem` file).
- Acquired non-volatile disk images in multiple formats (Raw, E01, SMART, AFF).
- Generated log file with acquisition details and verified hash values.

---

## Conclusion
FTK Imager is a versatile tool for acquiring both volatile and non-volatile evidence.  
By capturing memory dumps and forensic disk images while preserving integrity with write blockers and hash verification, investigators can ensure admissible and reliable digital evidence.


