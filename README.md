# week-1
Practice Assignments
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
