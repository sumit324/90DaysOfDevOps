##   understand how Linux works under the hood. short note that explains:

## 1) The core components of Linux (kernel, user space, init/systemd) ?
ANS -- The Everything in Linux based on ASK Principle . the kernal is HEART of Linux OS ,the kernal is drive the All linux operating system the required coding file
process store in kernal 
 Kernal is Devlope in C language 
 then developer is communicate with the kernal with the help of shell. shell is the gatway to communicate with the kernal.
 Shell is the Terminal (Shell Commands).
 Loaded into memory when the system boots , Talks directly to hardware
 What the Kernel does in real life ?
Decides which process gets CPU, Allocates RAM, Handles disk read/write, Manages network traffic, Controls drivers
## init / systemd (The Startup & Control Center)
 Every service you touch is controlled by systemd,
The first process started by the kernel, Always has PID 1 ,Modern Linux uses systemd 
WORKS -- Starts services during boot ,Stops services during shutdown, Restarts crashed services, Manages dependencies , Collects logs
## user space
 Area where users and applications run
 Shell (bash), Commands (ls, ps, top) , Applications (nginx, java, mysql, docker) it makes system calls to the kernel

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## 2) How processes are created and managedHow processes are created and managed ?
ANS -- A process starts when a command or program is executed, 
Steps -- User runs a command --> Kernel creates a process --> Process gets a unique PID
## process - 
    Running (R) → process is using CPU
    Sleeping (S) → waiting for input (disk, network, time)
    Stopped (T) → paused (Ctrl+Z)
    Zombie (Z) → finished but parent didn’t clean it
Process Management --> Kernel schedules processes using CPU time , Priority handled using nice values

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
## What systemd does and why it matters ?
ANS --  #WHAT --> Manages logs, Restarts failed services automatically , Starts services in parallel (fast boot)
        #WHY --> Almost all servers use systemd, Auto-restarting crashed apps, Managing dependencies between services

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## List 5 commands you would use daily 
ANS --> 
1)$cd = Change Directory (Folder) 
2)$top/htop = Check All Process 
3)$ls = view all file list 
4)$mkdir = Make Directory
5)$chmod = Change File Permission
6)$systemctl status = check server status 
















