# Experiment 02: Recover Deleted or Damaged Files Using TestDisk

## Objective
To recover deleted or corrupted partitions/files from storage devices using TestDisk.

## Tools Used
- TestDisk (CLI tool)
- Storage device with missing/corrupted partition

- <img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/fe101337-b0e4-40ab-a615-123e6f619aff" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/5feface6-59b6-4f9e-a217-c7e4fb871eba" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/2474367b-2a74-4998-a1b0-cc3988f416cb" />
<img width="601" height="927" alt="Image" src="https://github.com/user-attachments/assets/cc089680-2ab3-48ff-8fdd-0fd5443624de" />
<img width="1108" height="636" alt="Image" src="https://github.com/user-attachments/assets/b71fc9ea-aba4-4699-ba44-404d4b545685" />
<img width="1101" height="630" alt="Image" src="https://github.com/user-attachments/assets/80e09d5e-146b-41bb-9c0d-0a7b01b1c94d" />
<img width="1111" height="639" alt="Image" src="https://github.com/user-attachments/assets/7c82705f-6fd3-4fc6-b80e-b3d6add2db23" />

## Procedure
1. **Launch TestDisk** → Select target drive.
2. **Partition Table Detection** → Auto-detects type.
3. **Analyze Current Structure** → Check for errors/missing partitions.
4. **Quick Search** → Finds lost partitions.
5. **Deeper Search** → Scans cylinders for FAT/NTFS/ext backups.
6. **Partition Selection**:
   - Mark valid partition as Primary/Logical.
   - Mark damaged partitions as Deleted (D).
7. **Partition Table Recovery** → Save with **Write**.
8. **NTFS Boot Sector Recovery**:
   - Use **Backup BS** if primary boot sector is damaged.
   - Confirm copy of backup → Boot sector repaired.

---

## Result
- Successfully detected and recovered missing partitions.
- Restored NTFS boot sector from backup.
- Recovered files and verified integrity.

## Conclusion
TestDisk efficiently recovers lost partitions and repairs corrupted file systems, ensuring access to critical data.
