-------------------------------------------
Process Life cycle : 

1) New : creating process [IN_Disk]
    - the operating system allocates resources for 
    the process, including memory, CPU time, and 
    other system resources then it's called new
2) Ready : Process complete and ready to execute [in_RAM]
3) Runnig : Process is executing on memory [in_RAM]
4) Waiting : waiting for IO or beacause of Interrupt [in_RAM]
5) Terminated : Process finished and all RAM being Free 
    [Removed_all_allocated_resources]

[ 
    There are different OS modules which makes Process 
    go from one stage to another EX. schedule Dispatcher
    it give control of cpu to process from ready to running
]
- Context Switching: 
If the scheduler decides to switch to another 
process or if the current process enters a blocked 
state (e.g., waiting for I/O), a context switch occurs. 
During a context switch, the CPU saves the current 
process's execution state (registers, program counter, 
etc.) back to memory before loading the state of the 
next process to execute
-------------------------------------------
Process State Queues :
 -
1) Job Queue : NEW process queue. [IN_RAM]
2) Ready Queue : Ready Proocess [IN_RAM]
  - Degree Of multi-programming : how many processes
    can stay in Ready Queue at a time
- The ready queue is typically implemented as 
a data structure in memory, such as a priority 
queue or a FIFO queue
3) waiting Queue

------------------------------------------------
 How Process goes from one state to another ?
------------------------------------------------
1) Job scheduler/ Long_Term Schedular : 
- Moves Jobs from NEW to Ready state
  [ Program from DISK to RAM ]
- Jobs from Job Queue -> to Ready Queue
2) CPU shcedular/ Short_Term Schedular :
- Moves Jobs from Ready state to Running 
 [ Dispateches Jobs to CPU done by Schedular Dispatcher ]
3) for other states:
- there may be different component responsible for transition
the scheduler, I/O subsystem, and process management facilities.etc