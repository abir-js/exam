# 💻 Operating Systems (OS) Viva Preparation Guide

## 🔹 Basics of OS
**Q: What is an Operating System?**  
A: An OS is system software that acts as an interface between users and hardware, managing all system resources.

**Q: Functions of OS:**  
- **Process Management:** Handles process creation, scheduling, and termination.
- **Memory Management:** Allocates/deallocates memory to processes.
- **File System Management:** Organizes and controls data storage.
- **Device Management:** Controls and communicates with hardware devices.
- **Security and Protection:** Prevents unauthorized access to system resources.

## 🔹 Types of Operating Systems
- **Batch OS:** Executes batches of jobs without user interaction.
- **Time-Sharing OS:** Multiple users can use the system simultaneously.
- **Distributed OS:** Manages a group of distinct computers and makes them appear as one.
- **Network OS:** Manages network resources and users.
- **Real-Time OS:** Provides immediate response for time-critical tasks.
- **Multiprogramming:** Multiple programs in memory.
- **Multitasking:** CPU switches between tasks quickly.
- **Multiprocessing:** Multiple CPUs processing simultaneously.

## 🔹 Process Management
**Q: Process vs Program?**  
A: A program is a passive entity; a process is a running instance of a program.

**Q: Process States:**  
New, Ready, Running, Waiting, Terminated

**Q: PCB (Process Control Block):**  
Contains process-specific info like PID, PC, registers, scheduling info.

**Q: Context Switching:**  
Saving the state of a process and loading another process.

**Q: Threads:**  
- **User-level:** Managed without kernel.
- **Kernel-level:** Managed by OS kernel.

## 🔹 Scheduling Algorithms
- **FCFS:** Non-preemptive; executed in order of arrival.
- **SJF:** Shortest job executed first.
- **Round Robin:** Each process gets fixed CPU time.
- **Priority Scheduling:** Highest priority job first.
- **Multilevel Queue:** Processes are divided into queues.
- **Preemptive vs Non-Preemptive:** Preemptive allows interruption.
- **Gantt Chart:** Used to illustrate scheduling visually.

## 🔹 Interprocess Communication (IPC)
- **Shared Memory:** Common memory region.
- **Message Passing:** Via send and receive messages.
- **Pipes/FIFOs:** Used for data flow between processes.
- **Sockets:** IPC over network.
- **Signals:** Used to notify processes.

## 🔹 Deadlocks
**Q: Deadlock Conditions:**  
Mutual Exclusion, Hold and Wait, No Preemption, Circular Wait

**Q: Deadlock Prevention:**  
Break one of the four conditions.

**Q: Banker's Algorithm:**  
Avoids deadlock by checking safe state.

**Q: Detection & Recovery:**  
Use resource allocation graph, rollback or kill process.

## 🔹 Memory Management
- **Logical vs Physical Address:** Logical is virtual; physical is actual memory location.
- **Contiguous Allocation:** Single continuous memory block.
- **Paging:** Divides memory into fixed-size pages.
- **Segmentation:** Divides memory into logical segments.
- **Paging vs Segmentation:** Paging is fixed-size, segmentation is logical.
- **Virtual Memory:** Uses disk as extension of RAM.
- **Page Replacement Algorithms:**
  - FIFO: Oldest page replaced
  - LRU: Least recently used page replaced
  - Optimal: Page not used for longest time
  - LFU: Least frequently used
- **Thrashing:** Excessive paging causing low performance.

## 🔹 File System
- **File Attributes:** Name, type, size, etc.
- **File Operations:** Create, open, read, write, close, delete
- **File Allocation Methods:**
  - Contiguous: Consecutive blocks
  - Linked: Pointers to next block
  - Indexed: Index table for blocks
- **Directory Structures:** Single, Two-level, Tree, Acyclic
- **Inodes:** Index node in Unix file systems

## 🔹 Disk Scheduling
- **FCFS:** As requests come
- **SSTF:** Closest request next
- **SCAN/LOOK:** Elevator algorithm
- **C-SCAN/C-LOOK:** One-directional scan
- **Seek Time:** Time to move head
- **Rotational Latency:** Time to rotate disk

## 🔹 I/O Management
- **I/O Devices and Drivers:** Interface for hardware
- **Polling:** CPU checks I/O status
- **Interrupts:** Device notifies CPU
- **DMA:** Direct access to memory bypassing CPU

## 🔹 Security & Protection
- **Authentication:** Verifying identity
- **Authorization:** Granting permissions
- **Access Control Matrix:** Defines access rights
- **Encryption:** Securing data (symmetric/asymmetric)

## 🔹 System Calls
**Q: What are System Calls?**  
A: Interface between user and OS kernel.

**Types:**
- Process Control
- File Management
- Device Management
- Info Maintenance
- Communication

---

## 🔹 Common Viva Questions
- **Process vs Thread?** Thread is lightweight unit inside a process.
- **Context Switching?** Saving and restoring states during task switch.
- **Critical Section?** Code that accesses shared resources.
- **Preemptive vs Non-Preemptive Scheduling?** Preemptive interrupts, non-preemptive does not.
- **Paging and Segmentation?** Memory division methods.
- **System Call?** Function for user to interact with OS.
- **Thrashing?** Frequent paging causing slowdown.
- **Deadlock Avoidance?** Use algorithms like Banker's.
- **LRU Algorithm?** Replaces least recently used page.
- **Internal vs External Fragmentation?** Wasted space inside vs outside allocated memory.

---

> 📌 **Tip:** Visualize your answers (like drawing process states or memory blocks) when possible to impress the examiner!

