# PIC16F887 Password Security System

Simple password verification system implemented in **C** for the **PIC16F887** microcontroller.

The program reads a password from a keypad, displays messages on an LCD, and indicates the system state using **PORT E outputs**.

---

## Description

The system asks the user to enter a password using a keypad.  
The entered password is compared with a predefined password stored in the program.

Depending on the result, the system displays a message on the LCD and sets a value on **PORT E**.

Possible states:

| Condition | LCD Message | PORTE |
|----------|-------------|------|
| Correct password | `welcome` | `0x02` |
| Incorrect password | `try again` | `0x01` |
| 3 failed attempts | `blocked` | `0x04` |

---

## Default Password

The password defined in the program is:


1234


Defined in the code as:

```c
const char password[5] = {'1','2','3','4',0};
