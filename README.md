# Non-blocking-programing - Chapter 1: LEDs and Push Button
## Description
### This is the first chapter of a non-blocking programming course, in this folder, it will be include:
### 1-Controlling the blinking debounce time of a single LED
### 2-Dimmable LED
### 3- Asynchronous blinking LEDs
### 4-Toggle switch 
### 5-Multiple task: Toggle switch + LEDs
## Objective
### Showing the fundation of non-blocking programming in order to achive multiple task without blocking the microcontroller 
## Learning notes: Use of "unsigned long" instead of "int" when using millis()
### A standard "int" is signed, meaning the very first bit is used as a +/- flag. This splits its range in half between negative and positive numbers.
### An unsigned variable throws away negative numbers completely. By ignoring negatives, the entire memory space is dedicated strictly to positive numbers, which doubles the maximum positive value it can hold.
### **Why int Fails with millis()**
### The millis() function counts milliseconds from the moment the Arduino turns on.
### 1 second = 1,000 ms
### 33 seconds = 33,000 ms
### If you store millis() inside a standard int, your variable will hit its maximum limit (32,767) in just under 33 seconds.
### When an integer hits its limit and you add 1 more to it, it suffers from integer overflow. It rolls over to its lowest negative number (-32,768). If your code is checking if (currentMillis - previousMillis >= interval), the math completely breaks, and your timers, motors, or safety cutoffs will freeze or glitch.

## Author
### **Harwell Mejia**
### Developed as a part of my embedded systems and Arduino learning journey, with tutoring and guidance of GEMINI and ChatGPT
