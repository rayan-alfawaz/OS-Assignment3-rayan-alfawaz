# 📝 MY_WORK: Student Information, Development Log, Reflection & Answers

> This is the **only file** your instructor reads to grade Parts 3 and 4 (documentation and video). Everything you write here must be **in your own words**.

---

## 🛑 STOP: Read This Before You Do Anything Else

> ### 1️⃣ Read the whole `README.md` first
> The `README.md` in this repository contains the full instructions: how this assignment continues Assignment 1, the Chapter 5 recap, class descriptions, feature specifications, question prompts and the video script. **If you skip it, you will lose marks.**
>
> ### 2️⃣ Understand the full code before answering any question
> Open `SchedulerSimulationSync.java` and read it **from top to bottom**. You must be able to explain what `SharedStats`, `ReadyQueue`, `CpuWorker`, `RaceWindow.pause()`, `ReentrantLock` and `Semaphore` do **before** you write a single answer in Parts B and C. **Run the original starter first** (it is intentionally broken) and **save its output**: you need it for Question 1 of Part C.
>
> ### 3️⃣ Use only the code of this repository
> Work **only** on `SchedulerSimulationSync.java` from this repository. Do **not** copy or paste code from your previous assignments.
>
> ### 4️⃣ Commit many times, not once
> A single commit, or all commits made in the last hour, costs you **-0.5 mark**. See the [Commit Rules](#-commit-rules-mandatory) below.

**How to use this file:**
1. Fill in your **Student Information** (below) right now.
2. Follow the steps in the **Work Roadmap** in order.
3. Update the **Development Log** *every time* you work on the assignment, not at the end.
4. Do not delete any section header. Replace the `[...]` placeholders with your own text.

---

## 👤 Student Information

> ⚠️ **WARNING:** Fill this in first. Your name and ID must match the student ID you set in `SchedulerSimulationSync.java` (line 304) and the one you say in your video.

| Field | Your Answer |
|-------|-------------|
| **Full Name** | [Rayan Ibrahim AlFawaz] |
| **Student ID** | [446050856] |
| **University Email** | [446050856@std.psau.edu.sa] |
| **GitHub Username** | [rayan-alfawaz] |
| **Repository Link** | [https://github.com/rayan-alfawaz/OS-Assignment3-rayan-alfawaz/tree/main] |
 
---

## 🎥 Video Link

**Video Link**: [https://drive.google.com/file/d/1bxej_t_7wPe_Zw9-x7qPohJKI5xDkI2h/view?usp=sharing]

> ⚠️ **WARNING:** The video must be **publicly accessible** ("Anyone with the link can view") on **Google Drive**, **YouTube (Unlisted or Public)** or any other cloud file-sharing system. A private, restricted or broken link counts as a **missing video (-1 mark)**.
>
> 💡 **TIP:** Open the link in a **private/incognito window** before you submit. If it asks you to log in or request access, it is not public.
>
> 📌 **NOTE:** The link goes in **this file only** (`MY_WORK.md`), **not** in `README.md`. Name your video file `StudentID_Assignment3_Demo.mp4`. It must last **2 to 3 minutes**.

---

## 🗺️ Work Roadmap (follow in this order)

| Step | What to do | Where | Marks |
|:----:|------------|-------|:-----:|
| 0 | Read `README.md`, read the full code, **run the original starter and save its output** (it fails on purpose) | Your IDE | – |
| 1 | Fork, rename, keep the repo **PUBLIC**, set your student ID (line 304), **commit** | GitHub + code | Part 1 (1) |
| 2 | Feature 1: Mutex lock on the ready queue, **commit** | Code | Part 2 (0.25) |
| 3 | Feature 2: Mutex lock(s) on the shared statistics, **commit** | Code | Part 2 (0.25) |
| 4 | Feature 3: Counting semaphore instead of busy waiting, **commit** | Code | Part 2 (0.5) |
| 5 | Development Log (5+ entries, different dates) | This file, Part A | Part 3 (0.5) |
| 6 | Reflection (4 questions) | This file, Part B | Part 3 (0.5) |
| 7 | Technical Answers (4 questions) | This file, Part C | Part 3 (0.5) |
| 8 | Record the video, upload it, paste the link above | Video + this file | Part 4 (1.5) |
| 9 | Final check, then submit the repo link on Blackboard | Blackboard | – |

> 💡 **TIP:** Tick each step off as you go. Do not leave the log, the reflection or the video for the last day.

---

## 🔁 Commit Rules (MANDATORY)

> ### ⚠️ MANY COMMITS ARE REQUIRED. A single bulk commit is penalized (-0.5 mark).

**Minimum: 4 meaningful commits. Aim for 7 or more.**

| # | Commit | Example message |
|:-:|--------|-----------------|
| 1 | Student ID set | `Set my student ID: 441234567` |
| 2 | Feature 1: Ready queue lock | `Feature 1: Protected the ready queue with a ReentrantLock` |
| 3 | Feature 2: Statistics locks | `Feature 2: Added locks to the shared statistics counters` |
| 4 | Feature 3: Semaphore | `Feature 3: Replaced busy waiting with a counting semaphore` |
| 5 | Development log entries | `Docs: Added development log entries 1-3` |
| 6 | Reflection and answers | `Docs: Completed reflection and technical answers` |
| 7 | Video link | `Docs: Added demo video link` |

**Rules:**
- ✅ **One commit per feature.** Do not put all three features in one commit.
- ✅ **Commit after each work session**, and after each part of this file.
- ✅ **Spread your commits over different dates.** Not all in one day.
- ❌ **Do not make all commits in the last hour** before the deadline (November 14, 2026).
- ❌ **No vague messages** like `done`, `update` or `final version`.

> 💡 **TIP:** Your commit history is checked and you **show it in your video** (at least 4 commits visible). Your development log dates should match your commit dates.
>
> 💡 **TIP:** **Use VS Code** (see *Recommended Development Environment* in `README.md` for the full setup). Sign in to GitHub in VS Code, then commit from the Source Control panel (Ctrl+Shift+G) → stage → write a message → Commit → Sync/Push. You can edit and commit this file the same way. **Pushing** matters: commits that are not pushed to GitHub are invisible to the instructor.

---

# Part A: Development Log (0.5 mark)

> ⚠️ **WARNING:** Minimum **5 entries**, spread over **different dates**. Five entries written on the same day, or written all at once at the end, will lose marks and look like a copy. Entry dates should be **between the start of the assignment and the deadline (November 14, 2026)**.
>
> 💡 **TIP:** Write an entry at the **end of each work session**, while you still remember what happened. It takes 5 minutes.
>
> 💡 **TIP:** Be specific. "Worked on the code" is a weak entry. "Added a `ReentrantLock queueLock` to `ReadyQueue` and wrapped the body of `poll()` in `lock()` / `try` / `finally { unlock() }`" is a strong one.
>
> 📌 **NOTE:** Each entry needs: date and time, what you did, details, challenges, solution, and time spent. Real challenges are fine (and expected). Do not invent fake ones.

## Example Entry (do not copy it, write your own)

### Entry 1 - [November 2, 2026, 4:30 PM]
**What I did**: Forked the repository, set my student ID, and ran the original starter

**Details**:
- Forked the starter repository and renamed it
- Changed student ID on line 304 to my actual ID (441234567)
- Ran the original program: 4 CPUs started, three of them picked `P1`, then `IllegalThreadStateException` and the watchdog stopped the program
- Saved the output in a text file for Question 1
- Committed and pushed: `Set my student ID: 441234567`

**Challenges**: I did not understand why the same process was picked by three CPUs

**Solution**: Read `ReadyQueue.poll()` again and found the `RaceWindow.pause()` between reading the head and removing it

**Time spent**: 45 minutes

---

## Your Development Log

### Entry 1 - [November 4, 2026, 8:00 PM]
**What I did**: Forked the repository, setup environment, and tested the starter code.

**Details**:
- Forked the repo and changed the student ID to my actual ID (446050856).
- Ran the original starter code to observe the intentional failures.
- The program crashed immediately with a `NullPointerException` inside the `ReadyQueue.snapshot()` method, and the watchdog reported mismatched expected values.

**Challenges**: I was confused by the terminal output and why the crash happened inside `LinkedList`.

**Solution**: Analyzed the error trace and realized two CPU threads were accessing the shared ready queue simultaneously (one polling, one snapshotting) causing a `ConcurrentModificationException`.

**Time spent**: 45 minutes

---

### Entry 2 - [November 5, 2026, 4:15 PM]
**What I did**: Implemented Feature 1 (Mutex lock on Ready Queue).

**Details**:
- Added a `ReentrantLock` named `queueLock` to the `ReadyQueue` class.
- Protected all accesses to the `list` and `map` inside `add()`, `poll()`, `processOf()`, and `snapshot()` methods using `lock()` and `try/finally { unlock(); }`.
- Ran the simulation: the crashes stopped entirely, but the verification block still showed mismatches (e.g., observed 0 for context switches).

**Challenges**: Ensuring that the `unlock()` in the `poll()` method was correctly placed so it executes even when the method returns early.

**Solution**: Always placed `unlock()` inside the `finally` block, leaving the `return` statements safely inside the `try` block.

**Time spent**: 1 hour

---

### Entry 3 - [November 6, 2026, 5:30 PM]
**What I did**: Implemented Feature 2 (Mutex locks on Shared Statistics).

**Details**:
- Analyzed `SharedStats` and decided to use fine-grained locking: one independent lock for each of the three variables to maximize concurrency.
- Created `contextSwitchLock`, `completedProcessLock`, and `serviceTimeLock`.
- Protected the three writer methods (`increment...`) and the three reader methods (`get...`).
- Ran the code: the first three lines in the verification block now correctly show ✔.

**Challenges**: Remembering to lock the "getters" (readers) as well as the "setters", because a read during a write is also a race condition.

**Solution**: Added `try/finally` blocks to all getter methods with their respective locks.

**Time spent**: 1 hour

---

### Entry 4 - [November 7, 2026, 7:00 PM]
**What I did**: Implemented Feature 3 (Replaced busy waiting with a Counting Semaphore).

**Details**:
- Added a `Semaphore availableProcesses = new Semaphore(0)` in `ReadyQueue`.
- Called `release()` in the `add()` method whenever a new process is added.
- In `CpuWorker`, removed the `Thread.sleep(20)` loop (busy waiting) and replaced it with `availableProcesses.acquire()`.
- Implemented a clean shutdown by having the last finishing CPU release enough permits to wake up all remaining sleeping CPUs.

**Challenges**: The CPUs were getting stuck at the end of the simulation, causing the watchdog to trigger because they were waiting forever on an empty queue.

**Solution**: Added a broadcast `release(totalCPUs)` when `completedProcessCount == totalProcesses` to wake everyone up.

**Time spent**: 1.5 hours

---

### Entry 5 - [November 7, 2026, 9:00 PM]
**What I did**: Code documentation and preparing MY_WORK answers.

**Details**:
- Added English explanatory comments for Feature 1, 2, and 3 in the code.
- Verified that `Busy-waiting polls` is strictly 0 and all verification checks are green.
- Filled out the Development Log in `MY_WORK.md` and started drafting the technical reflection answers.
- Committed these documentation updates to GitHub.

**Challenges**: Explaining the concepts clearly in English and ensuring I fully understood why the semaphore's initial value must be 0.

**Solution**: Reviewed the Chapter 5 slides on Producer-Consumer problems to solidify my understanding before writing the answers.

**Time spent**: 1 hour

---

## Development Log Summary

> 💡 **TIP:** Fill this in **last**, after all entries are written.

**Total time spent on assignment**: 5 hours

**Most challenging part**: Managing the clean shutdown of threads in Feature 3. If the final wake-up signal was missed, the whole system would hang in a deadlock-like state.

**Most interesting learning**: Seeing how much CPU power is wasted on busy-waiting (thousands of empty polls) and how elegantly a Semaphore solves it by putting the threads to sleep.

**What I would do differently next time**: I would plan the lock granularity (Feature 2) on paper before typing the code, to clearly visualize which threads need access to which variables.

---

# Part B: Reflection (0.5 mark)

> 🛑 **STOP:** Do **not** start this part until you have read the `README.md`, read the **entire** `SchedulerSimulationSync.java`, run it, and finished the three features.
>
> ⚠️ **WARNING:** Each answer must be **5 to 7 sentences**, in **your own words**. Copied or AI-generated answers without understanding get **0 marks for the whole assignment**. You may be asked to explain them in person.
>
> 💡 **TIP:** Mention concrete things you actually did: a method you wrote, an error you hit, a line of output you saw. Generic answers score low.
>
> 💡 **TIP:** Draft your answer in a few bullet points first, then turn them into sentences.

## Question 1: What did you learn about synchronization?

> 💡 **TIP:** Talk about race conditions (read-modify-write), critical sections, mutual exclusion with `ReentrantLock` and `try/finally`, the role of a counting semaphore, and what surprised you when the starter failed.

**Your Answer:** *(5-7 sentences)*

[Through this assignment, I learned how easily race conditions can silently corrupt shared data when multiple CPUs execute concurrently. I saw firsthand how a lost update occurs when threads read and write to the same variable, like the contextSwitchCount, without proper protection. I learned to identify these critical sections and protect them using ReentrantLock in a try/finally block to ensure mutual exclusion safely. Furthermore, I understood the importance of lock granularity, realizing that using independent locks for independent variables maximizes the overall system performance. Finally, I learned how a counting Semaphore effectively puts threads to sleep, preventing the massive waste of CPU cycles caused by busy waiting on an empty queue.]

## Question 2: What was the most challenging part of this assignment?

> 💡 **TIP:** Pick **one** specific challenge (understanding why the starter failed, choosing the lock granularity, the initial value of the semaphore, the shutdown of the CPUs, Git, the video) and say *why* it was hard.

**Your Answer:** *(5-7 sentences)*

[The most challenging part of this assignment was implementing the clean shutdown logic for the CPU threads in Feature 3. Initially, I simply replaced the busy-waiting sleep with a semaphore acquire() call, which worked perfectly while processes were still running. However, when the simulation reached the end and all processes were completed, the remaining CPUs stayed blocked forever because the ready queue was permanently empty. It was difficult to figure out exactly when and how to wake up these sleeping threads without causing a race condition or breaking the loop early. This deadlock-like situation caused the watchdog timer to stop the program, failing the verification. I had to carefully think about broadcasting a final wake-up signal using release(totalCPUs) to ensure all threads could exit their methods properly.]

## Question 3: How did you overcome the challenges you faced?

> 💡 **TIP:** Describe your method: reading the slides and the documentation, adding `System.out.println` to debug, running the program many times, re-reading the README, testing after each small change, asking for help.

**Your Answer:** *(5-7 sentences)*

[I overcame these synchronization challenges by taking a systematic, step-by-step approach to testing and debugging. Instead of writing all the features at once, I implemented one lock at a time and ran the simulation repeatedly to isolate where the remaining errors were coming from. I heavily relied on the Chapter 5 course slides to understand the theoretical difference between mutex locks and semaphores before writing the Java code. Whenever the watchdog timer triggered or a deadlock occurred, I analyzed the console output to trace which CPU was polling the queue. I also reviewed the Java documentation for ReentrantLock and Semaphore to understand how their methods interact under the hood. Finally, I made sure to strictly follow the assignment hints about placing unlock() inside finally blocks to guarantee locks are always released securely.]

## Question 4: Where can synchronization concepts be applied in real-world applications?

> 💡 **TIP:** Use real applications you know (banking and money transfers, ticket or seat booking, a shared counter on a website, a print queue, a database) and connect each one to what you built here (shared data, critical section, lock or semaphore).

**Your Answer:** *(5-7 sentences)*

[The synchronization concepts I applied here are essential for building any robust real-world backend software system. For example, in a banking application, mutex locks are absolutely critical to prevent race conditions when two users try to transfer money from the same account simultaneously. If the balance update is not mutually exclusive, the bank could easily lose money due to a lost update just like our shared statistics did. Another great application is an online ticket booking system, where a counting semaphore can represent the exact number of available seats. When a user books a ticket, they acquire a permit, ensuring the system never oversells tickets to concurrent users. Finally, these concepts are vital for database management systems, where multiple queries must safely read and write to the same tables without causing deadlocks.]

### Optional: What would you like to learn more about?

[Any topics related to synchronization or operating systems that you're curious about?]

### Optional: How confident do you feel about synchronization concepts now?

[Beginner / Intermediate / Confident. What do you understand well? What needs more practice?]

### Optional: Feedback on the assignment

[Any comments? Was it helpful? Too easy or hard? Suggestions?]

---

# Part C: Technical Answers (0.5 mark)

> 🛑 **STOP:** You cannot answer these questions without understanding the code. Re-read `SchedulerSimulationSync.java` and **run it** first. Your answers must reference **your own code and your own output** (your student ID makes your output and your expected values unique).
>
> ⚠️ **WARNING:** Each answer must be **3 to 5 sentences**, with specific examples from your code or output. Use correct terms: race condition, critical section, mutual exclusion, mutex lock, semaphore, busy waiting, deadlock, producer, consumer.
>
> 💡 **TIP:** Keep the output of the **original starter** and the output of your **final version** in text files or screenshots, so you can copy real snippets for Question 1.

## Question 1: Race Condition in Your Own Output

**Question**: Run the **original starter** (before any fix) and paste the **verification block** of that run. Which value was wrong (expected vs observed)? Explain **step by step**, with two named threads/CPUs, how **one lost update** happens on one of the shared variables (read, `RaceWindow.pause()`, write). Why can the same bug happen on a real machine even without `RaceWindow`, and why is it hard to detect?

> ⚠️ **WARNING:** The snippet must come from **your own run** (with your student ID), not from a classmate or from this README.
>
> 💡 **TIP:** Use a small timeline: *CPU-1 reads `contextSwitchCount` = 12 → CPU-2 reads 12 → CPU-1 writes 13 → CPU-2 writes 13 → one increment is lost.* If your starter run crashed before printing numbers, run it several times (or paste the exception and the watchdog message and explain it).

**Your Answer:** *(3-5 sentences)*

[In my original starter run, the simulation failed because a ConcurrentModificationException crashed the threads before they could finish, leaving all observed statistics at 0 instead of their expected values (31 context switches, 18 completed processes, and 123533 ms service time). If the crash hadn't stopped execution, lost updates would occur on the shared counters due to the lack of mutual exclusion. On a real machine, this bug can happen without RaceWindow because the operating system can preempt a thread at the hardware level at any microsecond. It is notoriously hard to detect because it depends entirely on unpredictable thread scheduling, meaning the program might run flawlessly many times before silently corrupting the data.]

Verification block of the **original starter**:
```
[═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 31       observed 0        ✘ MISMATCH
  Completed processes                    expected 18       observed 0        ✘ MISMATCH
  Total service time (ms)                expected 123533   observed 0        ✘ MISMATCH
  Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
  ✘ At least one check failed (see the ✘ lines above): a race condition or busy waiting is still present.]
```

Verification block of **my final version**:
```
[═══ VERIFICATION (expected values are computed from YOUR seed) ═══
  Context switches (quanta executed)     expected 31       observed 31       ✔
  Completed processes                    expected 18       observed 18       ✔
  Total service time (ms)                expected 123533   observed 123533   ✔
  Busy-waiting polls (must be 0)         expected 0        observed 0        ✔
  ✔ All shared values are consistent.]
```

**Explanation of the timeline:**
[A lost update happens step by step as follows: CPU-1 reads contextSwitchCount (e.g., value is 10) and is then preempted by the OS during RaceWindow.pause(). Simultaneously, CPU-2 reads the exact same value (10). CPU-1 resumes, adds 1, and writes back 11. CPU-2 also adds 1 to its read value and writes back 11. One increment is permanently lost because both CPUs overwrote each other based on the same stale read.]

## Question 2: Critical Sections and Lock Granularity

**Question**: List the **critical sections** you protected (variables and methods) and the lock(s) you used. **Lock granularity:** did you use **one lock** for the three statistics or **one lock per variable**? Why, and what is the trade-off? Why is the **ready queue** protected by a **different** lock than the statistics? Explain how your solution provides **mutual exclusion**, and discuss **progress** and **bounded waiting** (a default `ReentrantLock` is not fair: what does that imply?).

> 💡 **TIP:** The three counters are independent: does updating `contextSwitchCount` need to block an update of `totalServiceTime`? Also think about what could go wrong (deadlock, or long waiting) if the queue lock and the statistics lock were the **same** lock and a thread held it while doing something slow.

**Your Answer:** *(3-5 sentences)*

[I protected the ready queue operations using a single ReentrantLock named queueLock, and the SharedStats counters using three independent locks (contextSwitchLock, completedProcessLock, and serviceTimeLock). I chose one lock per variable (fine-grained locking) to maximize concurrency, allowing different CPUs to safely update different statistics simultaneously without unnecessarily blocking each other. The ready queue requires a completely different lock to decouple queue management from statistics tracking, preventing overall performance bottlenecks. By using lock() and try/finally { unlock(); }, I ensured strict mutual exclusion; however, since a default ReentrantLock is not fair, it does not guarantee bounded waiting, meaning a heavily loaded thread could theoretically be starved.]

| Critical section (variable / method) | Lock used | Why it needs protection |
|---|---|---|
| [ReadyQueue: add(), poll(), processOf(), snapshot()] | [queueLock] | [To prevent ConcurrentModificationException and lost processes when multiple CPUs access the list and map simultaneously.] |
| [SharedStats: contextSwitchCount updates and reads] | [contextSwitchLock] | [To prevent lost updates during the read-modify-write cycle when CPUs log a new quantum.] |
| [SharedStats: completedProcessCount updates and reads] | [completedProcessLock] | [To ensure the simulation stops accurately without losing the final completion signal.] |
| [SharedStats: totalServiceTime updates and reads] | [serviceTimeLock] | [To accurately accumulate the sum of CPU time without race conditions.] |

## Question 3: Busy Waiting vs Semaphore

**Question**: Describe the **busy waiting** of the starter and its cost (give the `Busy-waiting polls` number from your **starter** run). What does the **value of your semaphore** represent? What is its **initial value** and why? What is its value right after the `numProcesses` initial `add()` calls? Why does the last CPU call `release(totalCPUs)` at the end, and what would happen if it did not?

> 💡 **TIP:** Think about what a CPU does when the queue is empty in the starter, and what a CPU does in your final version (is it running, ready or blocked?). Also check what happens to a CPU blocked in `acquire()` when no process will ever be added again.

**Your Answer:** *(3-5 sentences)*

[The starter code's busy waiting forced the CPUs to repeatedly poll an empty queue inside a while loop, checking if the thread was null and sleeping for 20ms, which pointlessly wasted thousands of CPU cycles. I replaced this with a counting semaphore whose value directly represents the exact number of processes currently waiting in the ready queue. Its initial value is 0 because the queue is completely empty at the start, and it becomes exactly 18 right after the main thread's initial add() calls. The last active CPU must call release(totalCPUs) to broadcast a clean shutdown signal; if it did not, the remaining CPUs would stay indefinitely blocked on acquire(), resulting in a hung program and a watchdog timeout.]

## Question 4: Classical Problems and Deadlock

**Question**: The CPUs and the ready queue look like a classical synchronization problem of Chapter 5. **Name it**, and say who plays the **producer** and the **consumer** roles (careful: here the CPUs also re-enqueue processes). If the ready queue were **bounded** (capacity `K`), name the **three semaphores** you would need and their **initial values**. Describe a **deadlock scenario** that appears if a thread acquired the **mutex before** waiting on the semaphore (or if two locks were acquired in different orders), and say **which of the four necessary conditions** you would break to prevent it.

> 💡 **TIP:** Recall the bounded-buffer solution of the slides (`empty`, `full`, `mutex`) and the order of `wait()` calls in the producer and the consumer. For the deadlock, think about a producer that holds the mutex while waiting for a free slot that only a consumer (who needs the mutex) can create.

**Your Answer:** *(3-5 sentences)*

**Classical problem and roles**:
[This is the classic Producer-Consumer synchronization problem. In our simulation, the CPUs uniquely act as both consumers (when they pull a process from the queue to execute) and producers (when they re-enqueue a process that hasn't finished its burst time).]

**Semaphores for a bounded queue (name and initial value)**:
[We would need three semaphores: 1) empty (initial value = K, counting available slots), 2) full (initial value = 0, counting available items), and 3) mutex (initial value = 1, ensuring mutual exclusion).]

**Deadlock scenario and prevention**:
[A deadlock would occur if a producer acquired the mutex first, then waited on the empty semaphore when the queue was entirely full; the consumer could never consume to free space because it needs the mutex held by the sleeping producer. We prevent this by breaking the "Hold and Wait" condition, enforcing a strict ordering where threads must acquire the scheduling semaphores (empty or full) before acquiring the mutex lock.]

## Summary

**Key concepts I understood through these questions:**
1.How race conditions silently corrupt data during read-modify-write operations at the microsecond level.
2.The importance of fine-grained locking to maximize concurrency without causing performance bottlenecks.
3.How counting semaphores efficiently eliminate busy-waiting by putting idle threads to sleep safely.

**Concepts I need to study more:**
1.Advanced deadlock avoidance algorithms in complex operating systems, such as the Banker's Algorithm.
2.How the lack of bounded waiting in default ReentrantLock implementations could theoretically cause thread starvation in massive applications.

---

# ✅ Final Checklist (complete before submitting)

> ⚠️ **WARNING:** Go through every line. Blackboard does not accept submissions after the deadline, which is **November 14, 2026**.

**Repository**
- [✅ ] Repository is **PUBLIC** (Settings → Danger Zone → Visibility)
- [✅ ] Repository is renamed to `OS-Assignment3-YourFirstName-YourLastName`
- [✅ ] GitHub account uses the university email (`@std.psau.edu.sa`)

**Code**
- [✅ ] Student ID is set in `SchedulerSimulationSync.java` (line 304)
- [✅ ] My code is based **only** on the starter of this repository (nothing copied from previous assignments)
- [✅ ] Code compiles and runs with no errors, and terminates by itself (no `⛔ WATCHDOG`)
- [✅ ] Feature 1 (ready queue lock), Feature 2 (statistics locks) and Feature 3 (semaphore, no busy waiting) all work
- [✅ ] **The four verification lines are ✔ in 5 consecutive runs**
- [ ✅] Every lock is released in a `finally` block
- ✅[ ] `RaceWindow`, `Config`, the verification block and the watchdog are **unchanged**
- [✅ ] Each feature has clear comments

**Commits**
- [✅ ] **At least 4 meaningful commits, ideally 7 or more**
- [ ✅] **One commit per feature**
- [ ✅] Commits are spread over **different dates** (not all in the last hour)
- [ ✅] Everything is **pushed** to GitHub

**This file (`MY_WORK.md`)**
- [✅ ] Full name and student ID filled in at the top
- [✅ ] Development log has **5+ entries** on different dates
- [✅ ] Reflection: 4 questions, 5-7 sentences each
- [✅ ] Technical answers: 4 questions, 3-5 sentences each, with examples from **your** output (starter output **and** final output pasted in Question 1)
- [✅ ] No `[...]` placeholders left
- [✅ ] No section headers deleted

**Video**
- [✅ ] 2-3 minutes long, named `StudentID_Assignment3_Demo.mp4`
- [✅ ] Shows your name, ID, repository, 3 features (and your lock granularity choice), IDE execution with the verification block, one synchronization concept, and commit history
- [ ✅] Link is **public** (tested in an incognito window) and pasted in the **Video Link** section above

**Blackboard**
- [ ✅] Submit **only** the link to your public GitHub repository

> 🎯 **Good luck!** Start early, commit regularly, and make sure you can explain every line you submit.
