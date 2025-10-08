# Cpp_Experiment_19_Queue-Implementation-using-Array

# 📘 Experiment: Queue Implementation Using Arrays in C++

---

## 🎯 AIM
To implement a queue data structure using arrays in C++ and perform basic operations such as **enqueue (add)**, **dequeue (remove)**, and **display**.  

---

## 📌 OBJECTIVES
- To understand the concept of a queue as a linear data structure.  
- To implement a queue using **arrays** and **classes** in C++.  
- To handle errors such as **queue overflow** and **underflow**.  
- To understand the **FIFO (First In, First Out)** principle used in queues.  

---

## 📖 THEORY

### 🔹 What is a Queue?
A queue is a linear data structure where elements are inserted at **rear** and removed from **front**.  

- **FIFO (First In, First Out):** The element added first is removed first.  
- Example: People waiting in line at a ticket counter – first person in line is served first.  

### 🔹 Basic Queue Operations
- **Enqueue (Add):** Insert element at the rear.  
- **Dequeue (Remove):** Remove element from the front.  
- **Display:** Show all elements in the queue.  

### 🔹 Real-Life Examples
- Ticket booking systems (first come, first served).  
- Printer queue (documents printed in order).  
- Call center support (calls answered in order).  
- CPU scheduling in operating systems.  

### 🔹 Overflow and Underflow
- **Overflow:** Queue is full and cannot add more elements.  
- **Underflow:** Queue is empty and cannot remove or display elements.  

### 🔹 Comparison: Array vs Linked List Queue

| Feature           | Array-based Queue         | Linked-list-based Queue       |
|------------------|-------------------------|-------------------------------|
| Memory Allocation | Fixed size (MAX_QUEUE)   | Dynamic, grows as needed      |
| Speed             | Fast (direct indexing)   | Slightly slower (pointer ops) |
| Memory Usage      | May waste memory         | Exact usage, extra for ptr    |
| Implementation    | Simple and easy          | More complex                  |

---

## ⚙️ ALGORITHMS

### 🔹 Enqueue (add(value))
1. Check if `rear == MAX_QUEUE - 1`.  
   - If yes → print `"Queue is full"` (overflow).  
2. If queue is empty (`front == -1`) → set `front = 0`.  
3. Increment `rear` and insert `value` at `arr[rear]`.  

### 🔹 Dequeue (remove)
1. Check if queue is empty (`front == -1` or `front > rear`).  
   - If yes → print `"Queue is empty"` (underflow) and return error code.  
2. Return `arr[front]` and increment `front` by 1.  

### 🔹 Display Queue (show)
1. If queue is empty (`front == -1` or `front > rear`) → print `"Queue is empty"`.  
2. Else → loop from `front` to `rear` and print all elements.  

---

## 📝 PROGRAM DESCRIPTION
The program defines a **class `Queue`** with:

**Private data:**  
- `arr[MAX_QUEUE]` → Array to store queue elements.  
- `front` → Index of the front element.  
- `rear` → Index of the rear element.  

**Public functions:**  
- `add(int value)` → To enqueue an element.  
- `remove()` → To dequeue the front element.  
- `show()` → To display all queue elements.  

**Main function:**  
1. Create a queue object.  
2. Add elements to the queue.  
3. Display current queue.  
4. Remove one element and print it.  
5. Display the queue after removal.  

---

## 🧩 CONCEPTS USED
- **Class & Object:** Encapsulation of queue operations.  
- **Array:** Stores elements sequentially.  
- **Encapsulation:** Private data accessed only via class methods.  
- **Conditionals (if-else):** Handles overflow/underflow.  
- **Loops (for loop):** Display all elements.  
- **Macros (#define):** For constants like `MAX_QUEUE` and `EMPTY_ERROR`.  

---

## ✅ CONCLUSION
- Successfully implemented a queue using arrays in C++.  
- Demonstrated the **FIFO principle** clearly.  
- Handled **overflow** and **underflow** conditions effectively.  
- Provides a foundation for advanced data structure applications like circular queues and priority queues.  
