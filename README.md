# Create a ram disk 

```bash
diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nobrowse -nomount ram://[xxx]`
```

where `[xxx]` is the size of the RAM disk in terms of memory blocks.

> **Notes**:
> 
> 2048 memory blocks correspond to 1MB. Thus, `[xxx]` = `[yyy]` * 2048, where `[yyy]` is the size in MB.

E.g. 

- ```diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nobrowse -nomount ram://2048`  ``` will create an 1MB RAM disk
- ```diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nobrowse -nomount ram://2097152`  ``` --> 1 GB
- ```diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nobrowse -nomount ram://4194304`  ``` --> 2 GB
- ```diskutil erasevolume HFS+ 'RAM Disk' `hdiutil attach -nobrowse -nomount ram://8388608`  ``` --> 4 GB
