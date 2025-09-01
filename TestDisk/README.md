**Ex.No:2 Recover deleted or damaged files from a storage device using
Test Disk**

**AIM :**

TestDisk step by step to recover a missing partition and repair a
corrupted one.

1\. Log creation\]/

  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

All hard drives should be detected and listed with the correct size by
TestDisk:

  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   Use up/down arrow keys to select your hard drive with the lost
    > partition/

![](media/image13.png){width="0.14583333333333334in"
height="0.14583333333333334in"} If available, use raw
device /dev/rdisk\* instead of /dev/disk\* for faster data transfer.

Partition table type selection

TestDisk displays the partition table types. ![menu partition table
type](media/image1.png){width="6.268055555555556in"
height="3.165277777777778in"}

  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   Select the partition table type - usually the default value is the
    > correct one as TestDisk auto-detects the partition table type.

-   Press Enter to Proceed.

Current partition table status

TestDisk displays the menus (also see [[TestDisk Menu
Items]{.underline}](https://www.cgsecurity.org/wiki/Running_TestDisk)).![Analyse](media/image8.png){width="6.267716535433071in"
height="3.1666666666666665in"}

  -----------------------------------------------------------------------
  ![menus](media/image3.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   Use the default menu \"Analyse\" to check your current partition
    > structure and search for lost partitions.

-   Confirm at Analyse with Enter to proceed.

Now, your current partition structure is listed. Examine your current
partition structure for missing partitions and errors.

  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

The first partition is listed twice which points to a corrupted
partition or an invalid partition table entry.\
Invalid NTFS boot points to a faulty NTFS boot sector, so it\'s a
corrupted filesystem.\
Only one logical partition (label Partition 2) is available in the
extended partition. One logical partition is missing.

-   Confirm at ***Quick Search*** to proceed.

Quick Search for partitions

+---------------------------------+-------+---------------------------+
| TestDisk displays the first     | -     | (click on thumb to        |
| results in real time.           |    ![ | display the image).       |
|                                 | quick |                           |
|                                 |     > |                           |
|                                 |  sear |                           |
|                                 | ch](m |                           |
|                                 | edia/ |                           |
|                                 | image |                           |
|                                 | 9.png |                           |
|                                 | ){wid |                           |
|                                 | th="0 |                           |
|                                 | .7291 |                           |
|                                 | 66666 |                           |
|                                 | 66666 |                           |
|                                 | 66in" |                           |
|                                 |       |                           |
|                                 |    >  |                           |
|                                 | heigh |                           |
|                                 | t="0. |                           |
|                                 | 36805 |                           |
|                                 | 55555 |                           |
|                                 | 55555 |                           |
|                                 | 6in"} |                           |
+=================================+=======+===========================+
+---------------------------------+-------+---------------------------+

During the ***Quick Search***, TestDisk has found two partitions
including the missing logical partition labeled ***Partition 3***.

  -----------------------------------------------------------------------
  ![first results](media/image6.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   Highlight this partition and press ***p*** to list your files (to go
    > back to the previous display, press q to Quit, Files listed in red
    > are deleted entries).

All directories and data are correctly listed.

-   Press Enter to proceed.

Save the partition table or search for more partitions?

  -----------------------------------------------------------------------
  ![menu search!](media/image12.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   ***When all partitions are available*** and data correctly listed,
    > you should go to the menu **Write** to save the partition
    > structure. The menu Extd Part gives you the opportunity to decide
    > if the extended partition will use all available disk space or
    > only the required (minimal) space.

-   ***Since a partition, the first one, is still missing***, highlight
    > the menu ***Deeper Search*** (if not done automatically already)
    > and press Enter to proceed.

A partition is still missing: Deeper Search

***Deeper Search*** will also search for FAT32 backup boot sector, NTFS
backup boot superblock, ext2/ext3 backup superblock to detect more
partitions,

  ------------------------------------------------------------------------------------------------------------------
  it will scan each cylinder        ![quick                                                  (click on thumb).
                                    search](media/image9.png){width="0.7291666666666666in"   
                                    height="0.3680555555555556in"}                           
  --------------------------------- -------------------------------------------------------- -----------------------

  ------------------------------------------------------------------------------------------------------------------

After the Deeper Search, the results are displayed as follows:\
The first partition ***\"Partition 1\"*** was found by using backup boot
sector. In the last line of your display, you can read the
message ***\"NTFS found using backup sector!\"*** and the size of your
partition. The \"partition 2\" is displayed twice with different size.\
**Partitions listed as D(eleted) will not be recovered** if you let them
listed as deleted. Both partitions are listed with status ***D*** for
deleted, because they overlap each other. You need to identify which
partition to recover.

  -----------------------------------------------------------------------
  ![results deeper
  search!](media/image14.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   Highlight the first partition Partition 2 and press ***p*** to list
    > its data.

  ----------------------------------------------------------------------------------------------------------------
  The file system of the upper logical partition (label ![damaged file                               (click on
  Partition 2) is damaged                               system](media/image4.png){width="0.3125in"   thumb).
                                                        height="0.1527777777777778in"}               
  ----------------------------------------------------- -------------------------------------------- -------------

  ----------------------------------------------------------------------------------------------------------------

-   Press q for Quit to go back to the previous display.

-   Let this partition Partition 2 with a damaged file system marked
    > as D(deleted).

-   Highlight the second partition Partition 2 below

-   Press p to list its files.

  -----------------------------------------------------------------------
  ![list files](media/image5.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

It works, your files are listed, you have found the correct partition!

-   Use the left/right arrow to navigate into your folders and watch
    > your files for more verification

***Note:*** FAT directory listing is limited to 10 clusters - some files
may not appear but it doesn\'t affect recovery.

-   Press q for Quit to go back to the previous display.

```{=html}
<!-- -->
```
-   The available status are Primary, \* bootable, Logical and Deleted.

Using the left/right arrow keys, change the status of the selected
partition from D(eleted) to ***L(ogical)***. This way you will be able
to recover this partition.

  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

Hint: read [***[How to recognize primary and logical
partitions?]{.underline}***](https://www.cgsecurity.org/wiki/Partition_recognition_primary_and_logical)\
Note: If a partition is listed \*(bootable) but if you don\'t boot from
this partition, you can change it to ***P***rimary partition.

-   Press Enter to proceed

Partition table recovery

It\'s now possible to write the new partition structure.\
***Note:*** The extended partition is automatically set. TestDisk
recognizes this using the different partition structure.

  -----------------------------------------------------------------------
  ![menu write](media/image7.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   If **all partitions are listed** and only in this case, confirm
    > at ***Write*** with Enter, y and OK.

Now, the partitions are registered in the partition table.

NTFS Boot sector recovery

The boot sector of the first partition named Partition 1 is still
damaged. It\'s time to fix it. The status of the NTFS boot sector is bad
and the backup boot sector is valid. Boot sectors are not identical.

  -----------------------------------------------------------------------
  ![backup bs](media/image2.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   To copy the backup of the boot sector over the boot sector,
    > select ***Backup BS***, validate with Enter, use y to confirm and
    > next OK.

More information about repairing your boot sector under [[TestDisk Menu
Items]{.underline}](https://www.cgsecurity.org/wiki/Running_TestDisk).
The following message is displayed:

  -----------------------------------------------------------------------
  ![after backup bs](media/image11.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

The boot sector and its backup are now both OK and identical: the NTFS
boot sector has been successfully recovered.

-   Press Enter to quit.

  -----------------------------------------------------------------------
  ![reboot](media/image10.png){width="6.268055555555556in"
  height="3.165277777777778in"}
  -----------------------------------------------------------------------

  -----------------------------------------------------------------------

-   TestDisk displays ***You have to restart your Computer to access
    > your data*** so press Enter a last time and reboot your computer.
