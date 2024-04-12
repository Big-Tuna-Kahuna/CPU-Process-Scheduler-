# CPU-Process-Scheduler-
This program is a simulation of a process scheduling system that models how different algorithms handle processes within an operating system. It uses a discrete event simulation approach, where events such as process arrivals, departures, and time slices are managed through a priority queue based on event time. Here's a breakdown of the major components of the code and its functionality:

Program Structure
Main Structures: The main data structures used are struct process for storing process details and struct event for scheduling and handling events related to processes.
Event Types: There are three types of events: ARR (arrival), TSO (time slice occurrence), and DEP (departure).
Process Scheduling Algorithms: Supports three algorithms: First Come First Serve (FCFS), Shortest Job First (SJF), and Round Robin (RR).
Functionality
main(): Initializes the simulation by reading command line arguments that determine the scheduling algorithm and parameters like arrival rate and burst time distribution.
schedule_event(): Manages the scheduling of events. It can create new events for process arrivals, handle the time slice for round robin scheduling, and manage process departures.
process_Arrival(), process_Depart(), process_TimeSlice(): These functions handle the different types of events. For example, process_Arrival() manages new processes entering the system, process_Depart() handles the removal of processes after completion, and process_TimeSlice() manages the allocation of CPU time in round robin scheduling.
firstComeFirstServe(), shortJobFirst(), roundRobin(): These functions implement the respective scheduling algorithms.
Simulation Flow
Initialization: Set up initial conditions, including the first process arrival.
Event Handling: Processes events sequentially based on their scheduled time. Each event type triggers specific actions in the system.
Report Generation: Outputs process completion details into a file for analysis, which can be imported into tools like Excel for further examination.
Compilation and Execution
Compile with a standard C++ compiler like g++. For example: g++ -o scheduling_simulation simulation.cpp
Run the program with appropriate command line arguments. Example: ./scheduling_simulation 1 0.1 0.06 0.2
Command Line Arguments
Argument 1: Scheduling algorithm (1 for FCFS, 2 for SJF, 3 for RR)
Argument 2: Arrival rate for generating processes
Argument 3: Seed for generating burst times
Argument 4: Quantum time for Round Robin scheduling
This simulation is useful for understanding how different process scheduling algorithms operate and their effects on process handling in a controlled environment. The data generated from the simulation can be used to analyze and compare the efficiency and performance of each algorithm.
