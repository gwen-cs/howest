# Lab 4.1 Hardware components

## Questions

1. What is Virtualization and containerization? A: Approach to upgrade the computer. B: Approach to run applications. C: Approaches to computing environments that isolate IT components from the rest of the physical system.< D: Approaches to computing environments to manage all resources.
> C

2. What manages one or more containers on a system?
> Container engine
3. What command runs an existing container?A: docker run mycontainer. B: docker inspect mycontainer. C: docker start mycontainer D: docker pull mycontainer.
> C
4. How is the interface called that uses commands to execute tasks?
> cli, command line interface
5. What is the least visible part of the Linux os? A: Shell - B: Kernel
> B
1. What is name of the part that Docker runs? A: Container - B: Image - C: Virtual Image - D: VM
> A
1. What is the difference between docker run and docker start? A: docker run creates a new container - B: docker run starts the image - C: docker start downloads an image
> A
2. With what character ends the Linux prompt?
> $
1. How can you adjust the behaviour of a command? With A: Options - B: Arguments
> A
1. What is the command to open the manual page of ls?
> man ls
1. With what command can you execute a single command as root?
> sudo
1. With this command: `ls /etc /bin` - is the output A: the directory listing of /etc/bin or B: the directory listing of /etc and /bin
> B
1. With CTRL - [answer] what stops the running command? A - B - C or D?
> C
2.  How many states has a bit?
> 2
1.  How many bits is a byte?
> 8
1.  Which filesystem does Ubuntu use?
> ext4
1.  What is the root directory of Linux?
> /
1.  Can you boot a computer without OS? (yes/no)
> yes
1. What doubles every 2 years according to Moore's law?
> Transistors
1. What is the difference between Von Neuman architecture or Harvard?<br>A: different I/O units<br>B: Different busses<br>C: Different CPU.
> B
1.  Is a keyboard a component? (yes/no)
> no
1.  Does a motherboard connect every part of a computer? (yes/no)
> yes
1.  How is temporary storage called?
> RAM
1.  With what connector is the CPU connected to the Motherboard?
> socket
1.  If the computer has more then 2 CPU's how is this called?
> multiprocessing
1.  With what does the OS communicate with a hardware component?
> driver

1. A file that is being saved on the hard disk is 35 KB. 
   - Calculate the size of that file on the disk knowing that it's using NTFS with the default cluster size.
> Default cluster size NTFS = 4KB  
> Calculate clusters 35/4 = 8,75 -> 9 clusters needed  
> Size file on disk = 9*4 = 36KB  
- Calculate the amount of slackspace caused by this file
> 36 - 35 = 1KB slackspace

1. A file that is being saved on the hard disk is 512 KB. 
- Calculate the size of that file on the disk knowing that it's using NTFS with the default cluster size.
> Default cluster size NTFS = 4KB  
> Calculate clusters 512/4 = 128 clusters needed  
> Size file on disk = 128*4 = 512KB  
- Calculate the amount of slackspace caused by this file  
> 512 - 512 = 0KB slackspace

1. How many MB/s is an PC4-19200 RAM module?
> 19200 / 8 = 2400MB/s


1. A user writes 60GB a day of data to a 600 TBW SSD. After how many years is the disk unusable to write data to?
> 600 TBW = max 600 TB written to the SDD
> 60GB a day = 60 * 365 = 21900GB a year : 21,9TB a year
> 600 / 21,9 = 27 years

1. How many data can a user write a day to an 200 TBW SDD in 5 years?
> 200 TBW in 5 years = 200/5 = 40TB a year  
> 40TB = 40.000GB  
> 40000 / 365 = 110GB a day  