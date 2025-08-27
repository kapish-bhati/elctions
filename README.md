# 🗳️ Election Algorithms in C – CS50 Projects

This repository contains implementations of **three different voting algorithms** — **Plurality**, **Runoff**, and **Tideman** — written in **C** as part of my coursework for **CS50: Introduction to Computer Science** from **Harvard University**.

Each program simulates an election and determines the winner(s) using different voting systems. These projects deepened my understanding of arrays, structs, loops, conditionals, and algorithm design in C.

---

## 📂 Project Structure

* [`plurality.c`](./plurality.c) – Implements the **Plurality Voting** system.
* [`runoff.c`](./runoff.c) – Implements the **Runoff Voting** (a.k.a. Instant-Runoff Voting).
* [`tideman.c`](./tideman.c) – Implements the **Tideman Voting** method (Ranked Pairs algorithm).

---

## ✅ Plurality Voting

🗳️ **Winner is the candidate with the most votes.**

### How it works:

* Voters each cast a single vote.
* Votes are tallied.
* The candidate(s) with the most votes win.
* Ties are allowed.

### Run:

```bash
clang -o plurality plurality.c -lcs50
./plurality Alice Bob Charlie
```

---

## ✅ Runoff Voting

🗳️ **Eliminates candidates in rounds until one has majority support.**

### How it works:

* Voters rank candidates in order of preference.
* If no one has a majority, the candidate(s) with the fewest votes are eliminated.
* Votes are redistributed based on next preference.
* This continues until one candidate secures a majority.

### Run:

```bash
clang -o runoff runoff.c -lcs50
./runoff Alice Bob Charlie
```

---

## ✅ Tideman Voting (Ranked Pairs)

🗳️ **Constructs a directed graph of wins without cycles.**

### How it works:

* Voters rank candidates by preference.
* Preferences are tallied into pairwise wins.
* Pairs are sorted by strength of victory.
* Pairs are “locked in” to form a graph, avoiding cycles.
* The source of the graph is declared the winner.

### Run:

```bash
clang -o tideman tideman.c -lcs50
./tideman Alice Bob Charlie
```

*Note: This file includes function stubs marked as `// TODO`. Completion of the logic was part of the CS50 problem set.*

---

## 💡 Skills Learned

* **Structs & arrays** for managing candidates and votes
* **String manipulation and comparisons**
* **Sorting & graph algorithms** (especially for Tideman)
* **Control flow, debugging, and modular code design**
* Applying **real-world election systems** in code

---

## 📚 Acknowledgements

These programs were built as part of **[CS50](https://cs50.harvard.edu/)** – Harvard University’s world-renowned **Introduction to Computer Science** course. Each program was a part of a graded problem set focused on algorithmic thinking and real-world applications in C.

---

## 👨‍💻 Author

**Kapish Bhati**
*CS50 Student | Aspiring Software Engineer*

---

Let me know if you'd like to generate a combined PDF version or want separate READMEs for each file.
