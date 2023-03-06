# Starve-free-Readers-Writers-Problem
The Reader-Writer's problem deals with synchronizing multiple processes which are categorized into 2 types namely:

Readers - They read data from a shared memory location
Writers - They write data to the shared memory location

# Starve-free-Solution
We will make use of three semaphores and an integer variable:
1.rdc_mutex, a semaphore(initialised to 1) which is used to ensure mutual exclusion when read_count is upadated i.e. when any readers or exit from the critical section.
2.wrt_mutex, a semaphore(initialised to 1) to ensure a writer process to not to access the shared memory when other processes are accessing the shared memory.
3.in_mutex, a semaphore(intialised to 1) common to both reader and writer processes which add reader and writer processes to the waiting queue when writer is accessing the shared memory.
4.read_count, an integer variable(initialised to 0) that keeps the track of how many reader processes are currently accessing the shared memory.
