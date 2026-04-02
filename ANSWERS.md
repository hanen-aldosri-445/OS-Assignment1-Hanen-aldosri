# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**

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

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?]

2. **Runnable**: [When does P1 become Runnable?]

3. **Running**: [When is P1 Running?]

4. **Waiting**: [When/why would P1 be Waiting?]

5. **Terminated**: [When is P1 Terminated?]

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]

**Description**: 
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

---

## Summary

**Key concepts I understood through these questions:**
1. 
2. 
3. 

**Concepts I need to study more:**
1. 
2. 
