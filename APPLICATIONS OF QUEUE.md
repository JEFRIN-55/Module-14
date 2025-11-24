# Exp.No:40  
## APPLICATIONS OF QUEUE

---

### AIM  
To write a Python program to implement CPU Process Scheduling using a queue.

---

### ALGORITHM  

1. Start the program.  
2. Define the function `CalculateWaitingTime(at, bt, N)`.  
3. Initialize a list `wt` of size `N` with all values set to 0.  
4. Set `wt[0] = 0` for the first process.  
5. Print the table header: "P.No.", "Arrival Time", "Burst Time", "Waiting Time".  
6. Print the values for the first process.  
7. For each process from index `1` to `N-1`:  
   - Calculate `wt[i] = (at[i - 1] + bt[i - 1] + wt[i - 1]) - at[i]`.  
   - Print the process number, arrival time, burst time, and waiting time.  
8. Initialize `total_waiting_time = 0`.  
9. Add up all waiting times.  
10. Calculate average waiting time as `average = total_waiting_time / N`.  
11. Print the average waiting time.  
12. Get burst times as input from the user for 5 processes.  
13. Call `CalculateWaitingTime()` with `at`, `bt`, and `N`.  
14. End the program.

### PROGRAM

```python
# Reg.No- 212223060104
# Name- JEFRIN INOLA J

def findWaitingTime(processes, n, bt, wt):
    wt[0] = 0

    for i in range(1, n):
        wt[i] = bt[i - 1] + wt[i - 1]

def findTurnAroundTime(processes, n, bt, wt, tat):
    for i in range(n):
        tat[i] = bt[i] + wt[i]

def findavgTime(processes, n, bt):
    wt = [0] * n  
    tat = [0] * n  
    total_wt = 0
    total_tat = 0

    findWaitingTime(processes, n, bt, wt)

    findTurnAroundTime(processes, n, bt, wt, tat)

    print("Processes  Burst time  Waiting time  Turn around time")

    for i in range(n):
        total_wt += wt[i]
        total_tat += tat[i]
        print(f"   {processes[i]} \t     {bt[i]} \t     {wt[i]} \t\t   {tat[i]}")

    print(f"\nAverage waiting time = {total_wt / n:.2f}")
    print(f"Average turn around time = {total_tat / n:.2f}")

if __name__ == "__main__":
    processes = [1, 2, 3]
    n = len(processes)

    print("Enter burst times for 3 processes:")
    t0 = int(input("Burst time for P1: "))
    t1 = int(input("Burst time for P2: "))
    t2 = int(input("Burst time for P3: "))
    burst_time = [t0, t1, t2]

    findavgTime(processes, n, burst_time)
```

### OUTPUT
![image](https://github.com/user-attachments/assets/64d58bb6-1960-4335-9a5a-75fcc46cc086)

### RESULT
Thus, the Python program to implement FCFS Process Scheduling using a queue was succesfully implemented and verified.
