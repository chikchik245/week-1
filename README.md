# week-1 
Practice Question(1)
# Deep Clone a Linked List with Random Pointer

## 📝 Problem Statement
You are given a singly linked list where each node contains two pointers:
- next: Points to the next node in the list
- random: Points to any node in the list (or null)

Your task is to create a *deep copy* of this list.  
That means you should create a new list where each node is a new object,  
and has the same value and same structure (both next and random pointers) as the original list.

### Input Format
- A head node of a singly linked list. Each node contains:
  - int val
  - Node* next
  - Node* random

### Output Format
- Return the head of the *deep cloned linked list*.

---

## 🔍 Example

*Input Linked List:*

Node1(val=7) → Node2(val=13) → Node3(val=11) → Node4(val=10) → Node5(val=1)

Random Pointers: Node2.random → Node1 Node3.random → Node5 Node4.random → Node3 Node5.random → Node1

*Expected Output:*  
A deep clone with same structure but *different memory references*.

---

## ✅ Verification
1. Values are identical  
2. next and random pointers point to corresponding new nodes  
3. Original and cloned lists are disconnected (changing one doesn’t affect the other)  

---

## 💡 Approaches

### 1. HashMap (O(N) space)
1. Clone all nodes & store mapping original → clone
2. Assign next and random using the map

### 2. O(1) Space (Interleaving)
1. Insert cloned nodes between original nodes
2. Copy random pointers
3. Separate original and cloned list

---

## ⏱ Complexity
- *Time:* O(N)  
- *Space:* O(1) (for interleaving) / O(N) (for hashmap)

---





Practice Question(2)
# Flood Fill Algorithm

Company Tag: Facebook


---

📌 Problem Statement

You’re given an image represented as a 2D matrix of characters, where each character represents a pixel color.

You’re also given:

the coordinates of a pixel (sr, sc)

a new color C

Your task is to perform a Flood Fill operation:

Change the color of the starting pixel and all connected pixels (4-directionally: up, down, left, right) having the same original color to the new color C.

Diagonal connections are not allowed.

---

🔹 Input Format

A 2D character matrix image[n][m] representing the image.

Two integers sr and sc representing the row and column of the starting pixel.

A character C representing the new color.

---

🔹 Output Format

The updated image matrix after applying the Flood Fill Algorithm.

---

🔹 Example

Input

image = [
  ['B', 'B', 'W'],
  ['W', 'W', 'W'],
  ['W', 'W', 'W'],
  ['B', 'B', 'B']
]
sr = 2
sc = 2
C = 'G'

Output

[
  ['B', 'B', 'G'],
  ['G', 'G', 'G'],
  ['G', 'G', 'G'],
  ['B', 'B', 'B']
]

Explanation

The pixel at (2, 2) is 'W'.

Flood fill changes all connected 'W' pixels to 'G'.

'B' pixels remain unchanged.



---

🔹 Constraints

1 <= rows, cols <= 100

C is an uppercase character.

The original image contains only uppercase characters.



---

🔹 Approaches

Two common approaches can be used:

1. DFS (Depth First Search)


2. BFS (Breadth First Search)



Practice Question(3)
📌 Find the Greatest Common Divisor (GCD) of N Numbers

💼 Company: Amazon


---

📖 Problem Statement

In large-scale systems, finding a common pattern or factor among multiple datasets is often required for optimization. Similarly, in number theory, the Greatest Common Divisor (GCD) helps determine the largest number that divides a set of numbers without leaving a remainder.

Your task is to compute the GCD of n integers efficiently.


---

🔹 Input Format

First line: integer n (number of integers).

Second line: n integers separated by space.


🔹 Output Format

A single integer representing the GCD of the given numbers.



---

📝 Examples

Example 1

Input

3
42 56 14

Output

14

Explanation

Factors of 42 → {1, 2, 3, 6, 7, 14, 21, 42}

Factors of 56 → {1, 2, 4, 7, 8, 14, 28, 56}

Factors of 14 → {1, 2, 7, 14}

Greatest common factor = 14



---

Example 2

Input

4
8 16 32 64

Output

8


---

🔹 Constraints

1 ≤ n ≤ 10^5

1 ≤ arr[i] ≤ 10^9



---

⚡ Approach

We use the Euclidean Algorithm:

For two numbers:

gcd(a, b) = gcd(b, a % b)

For multiple numbers:

result = arr[0]
for i in range(1, n):
    result = gcd(result, arr[i])


⏱ Time Complexity: O(n log M) (where M is the largest number).
📦 Space Complexity: O(1)








---





