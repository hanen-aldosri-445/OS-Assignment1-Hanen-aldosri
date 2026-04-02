# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**A process is a program that runs independently with its own memory and resources.
A thread is a smaller part of a process that shares the same memory and resources with other threads in the same process.
The main difference is that threads are lighter and faster to create than processes because they don’t need separate memory.
In this assignment, we used threads so that all processes can share data easily and switch quickly without extra overhead.
Threads are more suitable for simulating CPU scheduling because they act like small tasks running in the same program.

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**

[In Round-Robin scheduling, if a process does not finish within its time quantum, it is temporarily stopped and then placed back at the end of the ready queue. This means the process will not continue immediately, but it will wait for the other processes to execute first, and then it will get another turn when it reaches the front of the queue again.
In my program, this behavior is clearly shown when a process prints that it yields the CPU, and then it gets added again to the ready queue..]

Example from my output:
```
[P1 completed quantum 3000ms │ Overall progress: [██████░░░░░░░░░░░░] 30%
Remaining time: 5000ms
↻ P1 yields CPU for context switch

➕ P1 (Priority: 4) added to ready queue │ Burst time: 8000ms]
```

**Explanation of example:**
[In this example, process P1 ran for one time quantum (3000ms), but it did not finish because it still has remaining time (5000ms). After that, the program shows that the process yields the CPU, which means it stops running.

Then, the process is added again to the ready queue, which means it goes to the end of the queue and waits for its next turn. Later, after other processes execute, P1 will run again when it reaches the front of the queue.]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[In my simulation, each process (like P1) is implemented as a thread. The thread goes through several states during its lifecycle. Below is how process P1 moves through each state:]

1. **New**: [
P1 is in the New state when it is first created using:
Thread thread = new Thread(process);
At this point, the thread exists but has not started execution yet.]

2. **Runnable**: [
P1 becomes Runnable after it is added to the ready queue:
processQueue.add(thread);
In this state, the thread is ready to run and waiting for the CPU to schedule it.]

3. **Running**: [P1 enters the Running state when the scheduler starts it:
currentThread.start();
At this moment, the run() method is executed, and P1 begins using the CPU for its time quantum..]

4. **Waiting**: [P1 goes into the Waiting state during execution when:
Thread.sleep(stepTime);
This simulates the process execution and causes the thread to pause temporarily.
Also, after finishing its quantum and being re-added to the queue, it waits for its next turn.]

5. **Terminated**: [P1 reaches the Terminated state when it finishes all its execution (remaining time becomes 0).
This is shown in the output when:
✓ P1 finished execution!
At this point, the thread has completed its task and will not run again.]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Web Servers Handling Multiple Users]

**Description**: 
[A web server (like Google, YouTube, or any online platform) handles many user requests at the same time, such as opening pages, logging in, or loading data. Each request can be treated as a separate thread or process.
]

**Why Round-Robin works well here**: 
[Round-Robin is useful because it gives each request a fair and equal amount of CPU time. This prevents one request from taking too long and blocking others. As a result, all users get quick responses, and the system stays fair and responsive.
]

### Example 2: [Operating System Multitasking]

**Description**: 
[In an operating system like Windows or Linux, many applications run at the same time, such as a browser, music player, and file explorer. Each application is treated as a process or thread.]

**Why Round-Robin works well here**: 
[Round-Robin works well because it switches quickly between processes and gives each one a small time slice (time quantum). This makes the system feel like all applications are running at the same time smoothly, without freezing or delaying one program too much.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
