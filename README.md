# CFG → CNF & GNF Converter

This is a simple website that converts a Context-Free Grammar (CFG) into:
- Chomsky Normal Form (CNF)
- Greibach Normal Form (GNF)

It is useful for students learning Automata Theory and Compiler Design.

---

<img width="1919" height="974" alt="image" src="https://github.com/user-attachments/assets/39f987b4-8d26-4a13-a8a8-c8ceefffa1b5" />




## What is CFG?

CFG means Context-Free Grammar.

It has:
- Variables (like S, A, B)
- Terminals (like a, b)
- Rules (productions)

Example:
S → AB | a  
A → aA | ε  
B → b  

---

## What is CNF?

In CNF, rules look like:
- A → BC  
- A → a  

Steps to convert:
1. Remove ε (empty) productions  
2. Remove unit productions (A → B)  
3. Remove useless symbols  
4. Convert long rules into small ones  

---
<img width="1379" height="806" alt="image" src="https://github.com/user-attachments/assets/da8841a2-196e-4879-9b3d-c21c7965d91d" />


## What is GNF?

In GNF, rules look like:
- A → aX  

This means:
- Rule must start with a terminal (a, b, etc.)

Steps:
1. Convert CFG to CNF  
2. Remove left recursion  
3. Make sure every rule starts with a terminal  

---

<img width="1405" height="836" alt="image" src="https://github.com/user-attachments/assets/f222d4cd-da33-4d3c-bf42-a55f6bba27ec" />


## Features

- Convert CFG to CNF  
- Convert CFG to GNF  
- Simple and easy to use  
- Fast output  

---

## How to Use

1. Enter your grammar  
2. Click:
   - Convert to CNF  
   - Convert to GNF  
3. See the result  

---

## Tech Used

- HTML  
- CSS  
- JavaScript  

