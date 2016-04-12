#### CentOS 7 & Windows 7 Multi-Boot

I had a laptop with Windows 7 pre-installed. I used `MiniTool Partition Wizard Free Edition 9.1` to resize windows partition to create some free space on hard drive.

http://www.partitionwizard.com/free-partition-manager.html

I installed CentOS 7 on the empty partition. Windows partition was safe and untouched.

---

##### Using `cfdisk` command on CentOS, we can check all available partitions on the hard drive and identify all Windows Partitions (ntfs).

```
----------------------------------------------------------------------------------
                           cfdisk (util-linux 2.23.2)

                              Disk Drive: /dev/sda
                       Size: 320072933376 bytes, 320.0 GB
             Heads: 255   Sectors per Track: 63   Cylinders: 38913

    Name        Flags	   Part Type  FS Type          [Label]        Size (MB)
 ------------------------------------------------------------------------------
                                      Unusable                             1.05*
    sda1        Boot        Primary   ntfs	 [System Reserved]	 209.72*
    sda2                    Primary   ntfs             [C Drive]      178257.92*
    sda3                    Primary   xfs				2147.49*
    sda5        NC          Logical   LVM2_member                     139456.42*
                            Logical   Free Space                           0.36*






     [   Help   ]  [  Print   ]  [   Quit   ]  [  Units   ]  [  Write   ]


                               Print help screen
----------------------------------------------------------------------------------
```

