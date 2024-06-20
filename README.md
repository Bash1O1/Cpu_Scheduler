Cpu Scheduler

Cpu scheduling is a process by which the processor is allocated to diffirent process for efficient execution. Cpu scheduling process executes process on the basis of multiple algorithms which are:

First Come First Serve (FCFS)

First Come First Served (FCFS) is a scheduling algorithm in which the process that arrives first is executed first. It is a simple and easy-to-understand algorithm, but it can lead to poor performance if there are processes with long burst times. This algorithm is a non-preemptive algorithm. In FCFS scheduling, the process that arrives first is executed first, regardless of its burst time or priority. This can lead to poor performance, as longer running processes will block shorter ones from being executed. It is commonly used in batch systems where the order of the processes is important.

Shortest Process Next (SPN)

Shortest Process Next (SPN) is a scheduling algorithm that prioritizes the execution of processes based on their burst time, or the amount of time they need to complete their task. It is a non-preemptive algorithm which means that once a process starts executing, it runs until completion or until it enters a waiting state. The algorithm maintains a queue of processes, where each process is given a burst time when it arrives. The process with the shortest burst time is executed first, and as new processes arrive, they are added to the queue and sorted based on their burst time. The process with the shortest burst time will always be at the front of the queue, and thus will always be executed next.

Shortest Remaining Time (SRT)

Shortest Remaining Time Next (SRT) is a scheduling algorithm that is similar to the Shortest Process Next (SPN) algorithm, but it is a preemptive algorithm. This means that once a process starts executing, it can be interrupted by a new process with a shorter remaining time. The algorithm maintains a queue of processes, where each process is given a burst time when it arrives. The process with the shortest remaining time is executed first, and as new processes arrive, they are added to the queue and sorted based on their remaining time. The process with the shortest remaining time will always be at the front of the queue, and thus will always be executed next.

Round Robin with varying time quantum (RR)

Round Robin (RR) with variable quantum is a scheduling algorithm that uses a time-sharing approach to divide CPU time among processes. In this version of RR, the quantum (time slice) is not fixed and can be adjusted depending on the requirements of the processes. This allows processes with shorter burst times to be given smaller quanta and vice versa. The algorithm works by maintaining a queue of processes, where each process is given a quantum of time to execute on the CPU. When a process's quantum expires, it is moved to the back of the queue, and the next process in the queue is given a quantum of time to execute.

Installation

Clone the repository

Install g++ compiler and make

sudo apt-get install g++ make

Compile the code using make command

Run the executable file

Input Format

First Line:  It is either 'trace' for gaant chart or 'stats' for waiting time and turnaround time

second line: It consist of the the no. correspong to the algorithm you want to execute

FCFS (First Come First Serve) --> 1

RR (Round Robin) --> 2

SPN (Shortest Process Next) --> 3

SRT (Shortest Remaining Time) --> 4

HRRN (Highest Response Ratio Next) --> 5

FB-1, (Feedback where all queues have q=1) --> 6

FB-2i, (Feedback where q= 2i) --> 7

Aging --> 8

Round Robin and Aging have a parameter specifying the quantum q to be used. Therefore, a policy entered as 2-3 means Round Robin with q=3. Also, policy 8-2 means Aging with q=2.

third line: It consist of an integer which is the last number to shown on the timeline

Fourth line: It represents the no. of process you want to execute 

Fifth line: Start of description of processes. Each process is to be described on a separate line. For algorithms 1 through 7, each process is described using a comma-separated list specifying:

1- String specifying a process name
2- Arrival Time
3- Service Time





