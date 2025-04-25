# Analysis-of-the-Disk-Structure-using-Sleuth-Kit
Nmae:Vimala Rani A

Reg No:212223040240
## AIM:
To analyze the disk structure of a given disk image using Sleuth Kit tools in Kali Linux.

## DESIGN STEPS:
### Step 1:
Obtain or create a disk image file (e.g., disk.dd) to analyze. Open the terminal in Kali Linux.

### Step 2:
Use Sleuth Kit tools like mmls, fsstat, and fls to examine the partition layout, file system details, and file listing.

### Step 3:
Interpret the output of the tools to understand the disk structure, including partitions, sectors, and files.

## PROGRAM:
Sleuth Kit Disk Analysis Commands

 Option 1: Create a Sample Disk Image (for Testing)

Let’s create a 10MB blank disk image and simulate file system activity:

bash
cd ~/Downloads

# Step 1: Create an empty disk image
dd if=/dev/zero of=disk.dd bs=1M count=10

# Step 2: Format it with a file system (like FAT32)
mkfs.vfat disk.dd


## OUTPUT:

![Screenshot 2025-04-25 143425](https://github.com/user-attachments/assets/3a78c080-bc68-41ef-a262-46811fd3ead0)

### Create Disk
![Screenshot 2025-04-25 143434](https://github.com/user-attachments/assets/8aa3efef-2b17-4cfd-b108-03c4d6785b70)

### mmls 
bash
mmls disk.dd

### fls
bash
fls -f fat -o 0 disk.dd

![Screenshot 2025-04-25 143445](https://github.com/user-attachments/assets/1a929821-91a5-448c-bee1-f116a2fabc6a)


![Screenshot 2025-04-25 143456](https://github.com/user-attachments/assets/dc875ee0-05e2-4539-82d3-2f2f60c83a70)



![Screenshot 2025-04-25 143505](https://github.com/user-attachments/assets/f68528c4-0a27-4678-9aad-fae70216cd53)


![Screenshot 2025-04-25 143513](https://github.com/user-attachments/assets/6317ca0e-1fb4-4872-a578-e95aa6a2ede8)


## RESULT:
The analysis was performed successfully using Sleuth Kit, and the disk structure was understood in detail.
