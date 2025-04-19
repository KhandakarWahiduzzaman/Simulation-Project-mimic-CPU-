# Simulation-Project-mimic-CPU-
This simulation project mimics CPU, memory, and disk management for an operating system.

Note:
1. PID 1 is always the OS
2. PID starts from 2 and increases without reuse
3. CPU stores currentPID
4. I implemented Ready queue with a vector as std::vector<Process> (or priority queue with some     
     handling since priority queue doesn’t allow easy preemption)
5. When a new process is added or returned from disk, compare its priority to the one on CPU
6. Preempted if needed
7. Memory management - Worst Fit
   '''Cpp
   struct MemoryItem {
    unsigned long long itemAddress;
    unsigned long long itemSize;
    int PID;
};
using MemoryUse = std::vector<MemoryItem>;
   '''
9. gfg
