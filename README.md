# DS_Lab8 # Data Structures Lab 08 - Queue Implementations

## Overview
This lab contains Python implementations of different queue data structures with practical applications in service systems like banks and hospitals.

## Files
- `DS_lab08.ipynb` - Jupyter notebook with all queue implementations

## Queue Implementations

### 1. Basic Bank Queue (`BankQueue`)
- **Type**: FIFO (First-In-First-Out)
- **Data Structure**: `deque` from collections
- **Methods**:
  - `arrive(customer)` - Add customer to end of queue
  - `serve()` - Serve customer from front of queue
  - `show()` - Display current queue state

### 2. Priority Queue (`PriorityQueue`)
- **Type**: Priority-based (min-heap)
- **Data Structure**: `heapq`
- **Methods**:
  - `add_task(priority, task)` - Add task with numerical priority
  - `serve_task()` - Serve highest priority task (lowest number)
  - `show()` - Display current tasks

### 3. Sign-based Priority Queue (`SignPriorityQueue`)
- **Type**: Priority with symbolic signs
- **Priority Mapping**:
  - `+` → Priority 1 (Urgent)
  - `-` → Priority 2 (Normal)
- **Methods**:
  - `add_task(task, sign)` - Add task with +/- priority
  - `serve_task()` - Serve based on sign priority
  - `show()` - Display queue status

### 4. Hybrid Service Desk (`MixedServiceDesk`)
- **Type**: Combined urgent/normal system
- **Data Structures**:
  - Urgent: Min-heap for `+` customers
  - Normal: FIFO queue for `-` customers
- **Methods**:
  - `arrive(name, sign)` - Add customer with priority sign
  - `serve()` - Serve urgent first, then normal
  - `show()` - Display both queues

## Student Exercises
Each implementation includes TODO tasks:
1. Add more customers/tasks and serve them
2. Make interactive with user input
3. Observe serving order patterns
4. Analyze real-world applications

## Real-World Applications
- Bank customer service
- Hospital emergency triage
- Call center priority systems
- Task scheduling in operating systems

## Requirements
- Python 3.x
- Collections module
- Heapq module
- Jupyter Notebook

## Usage
Run each cell sequentially to see queue demonstrations and complete the student exercises.
BankQueue - Basic FIFO queue using deque  PriorityQueue - Priority-based queue using heapq  SignPriorityQueue - Queue with +/- priority signs  MixedServiceDesk - Hybrid system combining urgent (heap) and normal (FIFO) queues
