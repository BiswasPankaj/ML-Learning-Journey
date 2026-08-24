# GATE Computer Science - Subject & Revision Master Tracker

### Target Status Legend
- ⭕ **Not Started** | ⏳ **In Progress** | 🎯 **Theory Complete** | ✅ **Done** | ⚠️ **Needs Review**

| Subject | Topic / Sub-topic | Status | PYQ / Practice Accuracy (%) | Rev 1 (Day 3) | Rev 2 (Day 14) | Rev 3 (Day 30) | Last Revised | Notes / Weak Spots |
| :--- | :--- | :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **Data Structures** | Binary Search Trees & AVL Trees | 🎯 | 85% | ✅ | ⏳ | ⭕ | 2026-08-10 | Rotations on deletion need speed |
| **Data Structures** | Hashing & Collision Handling | ⏳ | 65% | ⏳ | ⭕ | ⭕ | 2026-08-12 | Quadratic probing formula traps |
| **Algorithms** | Asymptotic Analysis & Recurrences | ✅ | 90% | ✅ | ✅ | ✅ | 2026-07-28 | Master Theorem Case 3 exception |
| **Algorithms** | Dynamic Programming (0/1 Knapsack, LCS) | ⏳ | 50% | ⚠️ | ⭕ | ⭕ | 2026-08-13 | State transition equation setup |
| **Operating Systems** | CPU Scheduling Algorithms | ✅ | 88% | ✅ | ✅ | ⏳ | 2026-08-01 | Gantt chart tied-breaking rules |
| **Operating Systems** | Page Replacement & Belady's Anomaly | 🎯 | 75% | ✅ | ⏳ | ⭕ | 2026-08-11 | FIFO vs LRU frame count edge cases |
| **DBMS** | Normalization (3NF, BCNF Decomposition) | ⏳ | 60% | ⏳ | ⭕ | ⭕ | 2026-08-14 | Dependency preservation verification |
| **DBMS** | Transaction & Concurrency Control | ⭕ | 0% | ⭕ | ⭕ | ⭕ | - | Need to start Serializability |
| **Theory of Comp.** | DFA/NFA Minimization & Pumping Lemma | 🎯 | 80% | ✅ | ⏳ | 0 | 2026-08-09 | Myhill-Nerode equivalence relations |
| **Compiler Design** | LL(1) & LR(0)/SLR(1) Parsing | ⭕ | 0% | ⭕ | ⭕ | ⭕ | - | FIRST and FOLLOW sets practice |
| **Computer Networks** | IP Addressing & Subnetting | ✅ | 92% | ✅ | ✅ | ✅ | 2026-07-25 | Classless CIDR host calculation |
| **Computer Networks** | TCP Congestion Control & Window Size | ⏳ | 55% | ⚠️ | ⭕ | 0 | 2026-08-12 | Slow start vs congestion avoidance thresholds |
| **COA** | Pipeline Hazards & Speedup | 🎯 | 70% | ✅ | ⏳ | ⭕ | 2026-08-08 | Structural vs Data hazards stall counts |
| **Digital Logic** | Combinational Circuits (Mux, Decoders) | ✅ | 95% | ✅ | ✅ | ✅ | 2026-07-20 | Boolean minimization |
| **Engineering Math** | Eigenvalues & Linear Systems | 🎯 | 82% | ✅ | ⏳ | 0 | 2026-08-07 | Cayley-Hamilton application |
| **Discrete Math** | Recurrence Relations & Graph Theory | ⏳ | 68% | ⏳ | ⭕ | 0 | 2026-08-13 | Handshaking lemma & Planar graphs |






# GATE CS Mistake Log & Trap Database

### Error Category Codes
- **[CR] Conceptual Error:** Fundamental gap in understanding the core topic.
- **[CL] Calculation / Silly Mistake:** Arithmetic error, misreading units (e.g., Bytes vs bits), or incorrect substitution.
- **[MS] Misread Question:** Missed keywords like *NOT*, *At least*, *Incorrect statement*, or *MSQ options*.
- **[TR] Novel Trap:** Standard GATE trick (e.g., 0-indexed vs 1-indexed, inclusive vs exclusive bounds).

| ID | Subject | Topic | Question Source / Year | Error Type | The Exact Trap / Where I Went Wrong | Correct Approach / Key Takeaway | Solved Correctly On Re-test? |
| :---: | :--- | :--- | :--- | :---: | :--- | :--- | :---: |
| #001 | OS | Process Synchronization | GATE 2021 (Set 1) | **[CR]** | Confused counting semaphore value initialization with binary semaphore limits. | Negative semaphore value `-k` directly indicates `k` processes are blocked in the queue. | ✅ Yes |
| #002 | CN | Sliding Window Protocol | Mock Test 3 - Q42 | **[CL]** | Calculated bandwidth in Mbps but forgot to convert round-trip time from milliseconds to seconds. | Always unify units first: $RTT = 2 \times \text{Prop Delay}$. Check $\text{bits} \leftrightarrow \text{Bytes}$ before dividing. | ✅ Yes |
| #003 | COA | Memory Interfacing | GATE 2019 | **[TR]** | Missed that memory was *byte-addressable* instead of *word-addressable*. | Number of address lines depends on word size vs total capacity: $\text{Lines} = \log_2(\text{Total Bytes} / \text{Word Size})$. | ⏳ Pending |
| #004 | DS | Binary Heaps | Practice Set 5 | **[MS]** | Selected the option for Min-Heap deletion time instead of heapification cost from an unsorted array. | Heap building takes $O(n)$ time; single deletion/insertion takes $O(\log n)$. Read question stem twice! | ✅ Yes |
| #005 | DBMS | Relational Algebra | GATE 2023 | **[CR]** | Assumed Division operator ($\div$) returns tuples matching *any* divisor element rather than *all*. | Division ($\div$) represents "FOR ALL" (universal quantification). | ⏳ Pending |
| #006 | Discrete Math | Set Theory | Mock Test 5 | **[MS]** | Missed that the question asked for *Strictly Partial Order* instead of *Poset*. | Strict partial order is Irreflexive and Transitive (no self-loops permitted). | ✅ Yes |