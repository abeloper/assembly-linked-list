# 🖥️ Assembly Linked List - EMU8086

<div align="center">

![Assembly Language](https://img.shields.io/badge/Assembly-x86--16-red)
![EMU8086](https://img.shields.io/badge/EMU8086-Compatible-green)
![Microprocessor](https://img.shields.io/badge/Microprocessor-Course-blue)
![License](https://img.shields.io/badge/License-MIT-yellow)

**Your gateway to understanding how computers REALLY work!**

[![Try Web Simulator](https://img.shields.io/badge/TRY-Web_Simulator-8A2BE2)](https://your-username.github.io/linked-list-simulator)
[![Assembly Code](https://img.shields.io/badge/View-Assembly_Code-orange)](./linked_list.asm)

</div>

## 🎯 About This Project

Welcome to your first journey into the fascinating world of **Microprocessor Programming**!  
This isn't just code — it's a deep dive into how **data structures** work at the most fundamental level of computing.

### 🌟 What Makes This Special?

- ✅ Complete **Linked List Implementation** in pure x86 Assembly  
- ✅ Demonstrates **five different addressing modes**  
- ✅ Perfect for **microprocessor or assembly language courses**  
- ✅ Includes **robust error handling** and edge case management  
- ✅ Fully **commented and educational** source code  


## 🏗️ What We Built

```asm
; ============================================
; LINKED LIST OPERATIONS - EMU8086 VERSION
; ============================================

.MODEL SMALL
.STACK 100h

.DATA
NODE_DATA  DB 10 DUP(0)       ; Data for up to 10 nodes
NODE_NEXT  DB 10 DUP(0FFh)    ; Next index, 0FFh = NULL
HEAD       DB 0FFh            ; Head index
TAIL       DB 0FFh            ; Tail index
COUNT      DB 0               ; Node count
````

## 🎮 Features

| Operation         | Description             | Assembly Magic               |
| ----------------- | ----------------------- | ---------------------------- |
| 📥 **Insert**     | Add nodes to the list   | Direct memory manipulation   |
| 🗑️ **Delete**    | Remove nodes by value   | Pointer arithmetic           |
| 👁️ **Display**   | Traverse and show list  | Register indirect addressing |
| ⚡ **Menu System** | User-friendly interface | DOS interrupts               |

## 🎯 Addressing Modes Demonstrated

We showcase **FIVE different ways** to access memory:

### 1. 🎯 Direct Addressing

```asm
MOV HEAD, BL              ; Straight to memory!
MOV [head_ptr], AX        ; No intermediaries
```

### 2. 🔄 Register Indirect

```asm
MOV [SI + BX], AL         ; Using registers as pointers
MOV AL, [SI + BX]         ; Memory to register transfer
```

### 3. 📍 Based Addressing

```asm
LEA DX, MSG_MENU          ; Load effective address
LEA DX, MSG_SHOW          ; Calculate offsets dynamically
```

### 4. 📊 Indexed Addressing

```asm
MOV SI, OFFSET NODE_DATA  ; Base address setup
ADD SI, AX                ; Index calculation
MOV DL, [SI]              ; Array-like access
```

### 5. 🔢 Immediate Addressing

```asm
MOV BYTE PTR [SI + BX], 0FFh  ; Constants in instructions
SUB AL, 30h                   ; Direct value manipulation
```

## 🚀 Quick Start

### 🧩 Prerequisites

* **EMU8086** - x86 Assembly Emulator
* Basic understanding of **Assembly Language**

### ▶️ Running the Code

1. Download and install **EMU8086**
2. Copy the assembly code from [`linked_list.asm`](./linked_list.asm)
3. Paste into EMU8086
4. Click **“Emulate”**
5. Click **“Run”** and enjoy the magic!


## 🧪 Test Drive It!

Try this sequence:

```
1 → 5    (Insert 5)
1 → 3    (Insert 3)
1 → 7    (Insert 7)
3        (Display)
```

**Expected Output:**

```
Linked List: 5 -> 3 -> 7
```

## 🎓 Learning Objectives

This project helps you understand:

* 🧠 Memory management **without garbage collection**
* 🧩 Pointer manipulation at the **hardware level**
* 🧮 Data structure implementation **from scratch**
* ⚙️ **x86 architecture** and instruction set
* 💬 **DOS interrupts** for input/output


## 🔗 Related Projects

### 🌐 Web Simulator

Check out our **interactive web simulator** that visually demonstrates this assembly code in action!
👉 [Launch Simulator](https://your-username.github.io/linked-list-simulator)

### 📚 Course Materials

* Microprocessor Architecture
* Assembly Language Programming
* Data Structures in Low-Level Languages

## 🛠️ Technical Details

| Aspect                  | Specification                  |
| ----------------------- | ------------------------------ |
| **Architecture**        | x86 16-bit                     |
| **Assembler**           | EMU8086                        |
| **Node Capacity**       | 10 nodes                       |
| **Node Size**           | 2 bytes (1B data + 1B pointer) |
| **NULL Representation** | 0xFF                           |

## 🎉 Acknowledgments

* 🧩 **EMU8086** for the amazing assembly emulator
* 🎓 **Microprocessor Course** for the inspiration
* 🙌 **You**, for taking the time to understand low-level programming!

