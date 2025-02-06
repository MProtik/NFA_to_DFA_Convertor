# **NFA to DFA Conversion Algorithm Project**

## **📝 Overview**

This project demonstrates an algorithm that converts a **Non-deterministic Finite Automaton (NFA)** into a **Deterministic Finite Automaton (DFA)**, ensuring a **reduced transition function** for the DFA. This algorithm is essential in automata theory and formal languages, where the NFA is used to recognize a language, and the DFA is the more efficient, deterministic equivalent.

The conversion follows a formal process and produces a DFA that accepts the same language as the original NFA.

---

## **🔑 Key Concepts**

1. **NFA (Non-deterministic Finite Automaton)**: A finite automaton where for a given state and input symbol, there can be multiple possible next states or even no next state at all.
  
2. **DFA (Deterministic Finite Automaton)**: A finite automaton where for each state and input symbol, there is exactly one possible next state.

3. **5-Tuple Representation**:  
   An NFA is represented as a 5-tuple \( (Q, Σ, Δ, q_0, F) \), where:  
   - \( Q \) = Set of states  
   - \( Σ \) = Set of input symbols (alphabet)  
   - \( Δ \) = Transition function  
   - \( q_0 \) = Start state  
   - \( F \) = Set of final states

---

## **⚙️ Conversion Algorithm**

The algorithm to convert the NFA into a DFA involves the following steps:

### **Step 1: Initialize DFA States**
- Initially, the set of states for the DFA is empty: **Q’ = ɸ**.
- Add the start state \( q_0 \) of the NFA to the set of DFA states \( Q' \).

### **Step 2: Add New States Based on Transitions**
- For each state in **Q'**, examine the possible transitions for each input symbol (using the transition function of the NFA).
- For every state in the NFA, calculate the possible set of states that could be reached and add them to **Q'** if they are not already present.

### **Step 3: Identify Final States**
- The final states of the DFA will include all states that contain at least one of the NFA’s final states.

### **Note**:
- This algorithm focuses on the **reduced transition function** of the DFA, which optimizes the conversion process.

---

## **💻 How It Works**

This project implements the steps of the algorithm, converting an NFA (given as a 5-tuple) into a DFA and ensuring the transition function is minimized.

### **Example:**

Consider an NFA with the following parameters:
- States: \( Q = \{q_0, q_1, q_2\} \)
- Alphabet: \( Σ = \{a, b\} \)
- Transition function \( Δ \) where:
  - \( Δ(q_0, a) = \{q_0, q_1\} \)
  - \( Δ(q_1, b) = \{q_2\} \)
  - \( Δ(q_2, a) = \{q_0\} \)
- Start state: \( q_0 \)
- Final state(s): \( F = \{q_2\} \)

The algorithm would process these details and generate a corresponding DFA with minimized transitions.

---

## **⚙️ Installation and Usage**

To run the NFA to DFA conversion:

### **1. Clone the repository:**

```bash
git clone https://github.com/yourrepo/nfa-to-dfa-conversion.git
cd nfa-to-dfa-conversion
```

## 🚨 Disclaimer

This project is intended for **educational purposes** to demonstrate the conversion of an **NFA** to a **DFA**. The algorithm may require adjustments for different types of **NFA** representations.

