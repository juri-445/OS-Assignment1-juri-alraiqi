# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:**A process is an independent program with its own memory space, while a thread is a smaller unit of execution inside a process that shares the same memory. Threads are faster to create and require fewer resources compared to processes. In this assignment, threads were used because they allow efficient CPU scheduling simulation with lower overhead. Threads can communicate more easily since they share memory within the same process

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:**? P1 completed quantum 4000ms │ Overall progress: [██████████░░░░░░░░░░] 52%
     Remaining time: 3556ms
   
  ? P1 yields CPU for context switch
  In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved to the end of the ready queue and waits for its next turn. This allows the CPU to give other processes a fair chance to execute. The process will run again when it reaches the front of the queue in the next cycle. This behavior prevents one process from using the CPU for too long and improves fairness between processes.
  ? P1 added to ready queue │ Burst time: 7556ms
  P1 completed quantum 4000ms
Remaining time: 3556ms
P1 yields CPU for context switch
P1 added to ready queue
Ready Queue

[Write your answer here. Describe the specific behavior - where does the process go? When does it run again? Give an example from your actual program output showing a process that was re-queued.]

Example from my output:
```
[Paste a relevant snippet from your program output here showing a process being re-queued]
```

**Explanation of example:**
[Explain what's happening in the output snippet you pasted]

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**

[Write your answer here. For each state, explain when P1 enters that state during the simulation. Use your understanding of the code to trace through the lifecycle.]

1. **New**: [When is P1 in New state?] Process P1 is in the New state when the thread object is created but before calling the start() method. At this stage, the thread exists but has not begun execution yet

2. **Runnable**: [When does P1 become Runnable?] P1 becomes Runnable after calling the start() method. In this state, the process is ready to run and waits in the ready queue for its turn to be scheduled by the CPU.

3. **Running**: [When is P1 Running?] P1 becomes Runnable after calling the start() method. In this state, the process is ready to run and waits in the ready queue for its turn to be scheduled by the CPU.

4. **Waiting**: [When/why would P1 be Waiting?] P1 moves to the Waiting state when it temporarily pauses execution, such as during a context switch or when methods like sleep() or join() are used in the simulation. In this state, the process waits until it can continue execution again

5. **Terminated**: [When is P1 Terminated?] P1 enters the Terminated state after it finishes its execution completely and no longer needs CPU time. At this point, the thread lifecycle ends.

---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: [Name of application/scenario]
 Web Server
**Description**: A web server handles many user requests at the same time using multiple threads. Each request is processed as a separate thread so the server can respond to multiple users efficiently. This helps the system stay fast and prevents delays when many users access the server together.
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]

### Example 2: [Name of application/scenario]
Media Player Application
**Description**: A media player uses multiple threads to handle different tasks such as playing video, loading files, and responding to user controls like pause or volume changes. These tasks run at the same time to improve performance and user experience
[Describe the real-world scenario or application]

**Why Round-Robin works well here**: 
[Explain why Round-Robin scheduling is suitable. Consider fairness, responsiveness, predictability, etc.]
Round-Robin scheduling ensures that each request gets a fair amount of CPU time. It prevents one request from taking all CPU resources and improves responsiveness. This makes the server balanced and efficient when serving many clients at the same time. This is similar to our assignment simulation where each process gets equal time using the CPU.

Round-Robin scheduling allows each task to receive CPU time regularly, which keeps the video playing smoothly while still responding quickly to user actions. It ensures fairness between tasks and improves responsiveness. This behavior is similar to the scheduling simulation in our assignment where each process runs for a fixed time quantum before switching to another process.

---

## Summary

**Key concepts I understood through these questions:**
1.  I understood the difference between a thread and a process, especially how threads share memory and are faster to create and manage than processes.
2. I learned how Round-Robin scheduling works using a time quantum and how processes move back to the ready queue if they do not finish execution.
3.  I understood the different thread states such as New, Runnable, Running, Waiting, and Terminated and how a thread moves between these states during execution.

**Concepts I need to study more:**
1. 
2. 
