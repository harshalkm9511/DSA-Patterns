# Math & Observation Patterns

Mathematical and observation-based problems focus on identifying patterns, deriving formulas, constructing valid answers, or finding properties that eliminate the need for brute-force simulation.

---

# 1. Simulation → Formula

## Definition

Replace an **O(n)** or **O(n²)** simulation with a mathematical observation, recurrence, or closed-form formula.

### Recognition

- Large constraints (`10⁹`, `10¹⁸`)
- Simulation gives TLE
- Process follows a deterministic pattern
- Asked for maximum/minimum after many operations

### Core Problems

| Problem | Difficulty |
|----------|------------|
| Maximum Value of an Alternating Sequence | Medium |
| 390. Elimination Game | Medium |
| 441. Arranging Coins | Easy |
| 754. Reach a Number | Medium |
| 319. Bulb Switcher | Medium |

### Key Techniques

- Pattern Recognition
- Mathematical Observation
- Recurrence Relation
- Closed Form Formula
- Sequence Analysis

---

# 2. Constructive Algorithms

## Definition

Instead of searching for the answer, directly **construct any valid solution** that satisfies the given constraints.

### Recognition

- "Return **any** valid answer"
- Construct...
- Build...
- Generate...
- Rearrange...
- Valid String
- Valid Array
- Valid Permutation

### Core Problems

| Problem | Difficulty |
|----------|------------|
| Rearrange String to Avoid Character Pair | Easy |
| 942. DI String Match | Easy |
| 984. String Without AAA or BBB | Medium |
| 1405. Longest Happy String | Medium |

### Key Techniques

- Greedy Construction
- Character Placement
- Grouping Elements
- Direct Construction

---

# 3. Invariants

## Definition

Find a property (Invariant) that **never changes** after every operation and use it to simplify the solution.

### Recognition

- Repeated Operations
- Can Transform?
- Is it Possible?
- Minimum Operations
- Process repeats until condition is met

### Core Problems

| Problem | Difficulty |
|----------|------------|
| 991. Broken Calculator | Medium |
| 397. Integer Replacement | Medium |

### Key Techniques

- Invariant
- Monovariant
- Reverse Thinking
- Greedy Observation

---

# 4. Counting / Contribution

## Definition

Instead of simulating every operation, count the contribution of each element or frequency directly.

### Recognition

- Count...
- Number of...
- Contribution...
- Frequency...
- Occurrences...

### Core Problems

| Problem | Difficulty |
|----------|------------|
| 169. Majority Element | Easy |
| 136. Single Number | Easy |
| 1588. Sum of All Odd Length Subarrays | Easy |

### Key Techniques

- Frequency Counting
- Contribution Technique
- Prefix Counting
- Mathematical Counting

---

# 5. Parity (Odd / Even)

## Definition

The solution depends only on whether numbers are **Odd** or **Even**, rather than their exact values.

### Recognition

- Odd / Even
- Alternating
- Parity
- Coloring
- Chessboard
- Game Theory

### Core Problems

| Problem | Difficulty |
|----------|------------|
| 319. Bulb Switcher | Medium |
| 292. Nim Game | Easy |

### Key Techniques

- Odd-Even Observation
- Bit Manipulation
- Mathematical Proof
- Game Theory Basics

---

# Pattern Selection Guide

| If You See... | Think... |
|---------------|----------|
| Simulation causes TLE | Simulation → Formula |
| Return **Any** Valid Answer | Constructive Algorithms |
| Property Never Changes | Invariants |
| Count Instead of Simulate | Counting / Contribution |
| Odd / Even Matters | Parity |

---

# Recommended Learning Order

1. Simulation → Formula
2. Constructive Algorithms
3. Counting / Contribution
4. Parity
5. Invariants

Master these five patterns before moving to advanced topics like Number Theory, Combinatorics, and Game Theory.