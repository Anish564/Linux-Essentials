# Compression Tools Guide

## Installation
Install compress tools
```bash

yum install bzip2  
```

## bzip2 Commands
Compress the 'messages1' file
```bash
bzip2 messages1  
```
Compress all files starting with 'messages'
```bash
bzip2 messages* 
```
Compress all '.log' files in the directory
```bash
bzip2 *.log 
```

Uncompress 'messages1.bz2'
```bash
bunzip2 messages1.bz2 
```
Uncompress all 'messages' files
```bash
bunzip2 messages*  
```

Uncompress all compressed files
```bash
bunzip2 *   
```

## gzip Commands

Compress 'messages2' (similar to bzip2)
```bash
gzip -v messages2 
```
Compress all files in 'log/' directory recursively
```bash
gzip -vr log/
```
Uncompress all files in 'log/' directory recursively
```bash
gunzip -vr log/ 
```
## zip Commands
Create a zip file for the 'log' folder
```bash
zip -r log.zip log/ 
```

---

# Tar Command Guide

## Basic tar Commands

Create a tar archive
```bash
tar -cvf messages5.tar messages5
```
Extract files from archive
```bash
tar -xvf messages5.tar
```
 Compress a folder
```bash
tar -cvf log.tar log/
```

## Checking Folder Size
Check size of 'log' folder
```bash
du -h log  
```

## Creating Compressed Archives

Create and compress with gzip
```bash
tar -czvf messages8.tgz messages8 
```
Create and compress with bzip
```bash
tar -cjvf messages9.tgz messages9 
```

## Extracting Compressed Archives

Unzip bzip2 archive
```bash
bunzip2 messages6.tar.bz2
```
Compress a tar file using gzip
```bash
gzip messages2.tar
```
Check which compression method was used
```bash
file messages2.tar.gz
```


