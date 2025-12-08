# **ECEn 225 🖥️ Doorbell Starter Kit 6\-11 Finale**

Cael Dearden

Last Updated: December 8th, 2025

 

## **Table of Contents 📚**

1. [Display](#lab-06-display)

2. [File](#lab-07-file)

3. [Camera](#lab-08-camera)

4. [Client](#lab-09-client)

5. [Threaded Client](#lab-10-threaded-client)

6. [Doorbell](#lab-11-doorbell)

 

 

## **About 💭**

 

There are two main purposes of the ECEn 225 Starter Lab Introduction. The first one is to teach others what we have done in each lab, explain necessary descriptions of each lab, and include the usage instructions on how to use the entire project. This README file is also a test to show our capability of creating a README file. README files should be legible and contain information regarding the project and follow *markdown* formatting guidelines.

 

As this marks the end of the semester, the purpose of the ECEn 225 Doorbell Lab Finale is to implement code that makes a fully functional smart doorbell. Through this README I will teach you what we have done in each lab, explain the necessary descriptions of each lab, and include the usage instructions to replicate the project. This README file is also a show of our knowledge to create and show our abilities of industry-standard techniques. A README follows *markdown* formatting and convention. I will now go through five labs explaining the flow and timeline of the doorbell project.

 

## **Lab 06 Display**

 

### **Description**

 

Getting Started covered the basics in the ECEn 225 lab kit. Included in this kit was a Raspberry Pi Zero 2 W and attachments such as a camera and joystick. This lab familiarizes yourself with the necessary tools to construct the doorbell.

 

### *Usage Instructions*

 

In order to complete this lab, you need to flash and configure the Pi Z2W with Linux. Assemble the Raspberry Pi kit that includes the camera, screen, etc. Then, gain remote access through SSH to enter the Pi Z2W. Once that is done, choose your preferred programming software that can set up a C development environment. Set up [GitHub](https://github.com/) to download the necessary repositories. This allows access to future labs on the Pi.

 

#### *Change Log 🚀*

 

 

 

## **Lab 07 File**

 

### **Description**

 

Command Line introduces new Linux environments, commands, shortcuts, and applications for code. Instead of a traditional programming software, this lab uses the PC terminal to explore the text editor and traversing directory trees from the command line.

 

### *Usage Instructions*

 

First off, have access to a PC terminal. Inside the terminal, concepts from the [Linux Survival Tutorial](https://linuxsurvival.com/) are used to traverse the directories. Once you are familiar with the particular format and instructions, open the shell challenge in the folder *starter-labs/02-command-line*. There, uncompress the *challenge.tar.xz*. This challenge requires you to create multiple trees inside the specifications. Be sure to remember the hidden folders and files that are scattered between directories.

 

#### *Change Log 🚀*

 

 

## **Lab 08 Camera**

 

### **Description**

 

C Programming establishes how to compile a program using the widely accepted gcc (GNU Compiler Collection). To accomplish this, basic C syntax is explained along with the difference between standard data types. A combination of these skills introduce coding blocks such as printf.

 

### *Usage Instructions*

 

The program includes many different statements such as stdio.h (library header) and include (directive that has existing code). These statements instruct the code on what to do. Put `gcc -E simple.c > simple_preprocessed.txt` into the terminal. This compiles the precompiled version of the text file included in Lab 03. Pay attention to what formatting specifiers need to be used. Compile your own C code into simple_preprocessed.txt, simple.s, simple.o, simple_assembled.txt, and simple. Make sure to use the \-Werror flag to search for errors while compiling. This makes the output required to pass of the lab.

 

#### *Change Log 🚀*

 

 

 

## **Lab 09 Client**

 

### **Description**

 

Data Types & Strings is a continuation of C Programming. New data types in stdint.h are introduced to the user. The purpose of the lab is to implement strings in C efficiently and learn basic debugging techniques.  In the end, these skills help new programmers not make mistakes when picking data types.

 

### *Usage Instructions*

 

Each type of data has a certain size. In a 64-bit system, char is 1 byte, short is 2, int is 4, long is 8, and a float is 4. This is important to know for deciding what to use for data in this folder. The folder contains a set of functions that need to be implemented and pass off the test. Additionally, pay attention to the particular order of operations in C. Multiplication has a higher priority than a Logical AND or Conditional sign. Use this knowlege when dealing with `strlen()`, `sprintf()`, `strcpy()`, `strncat()`, and `strncmp()`. After all the instructions, you will implement 4 out of 7 functions. These use certain data types and order of operations. I recommend using for and while loops to iterate through the arrays to accomplish a goal like calculating circumference. I also recommend using a bitwise operator to determine if a bit is a one or zero. `custom_strings.c` focuses on string implementation. Complete each function to return some sort of output.

 

#### *Change Log 🚀*

 

## **Lab 10 Threaded Client**

 

### **Description**

 

Image is the final lab in the starter folder before any major implementations of the doorbell. Learn how to manipulate bytes in C to modify image files using BMP. Enum and structs are introduced and used commonly in controlling the aspects of an image. Multiple .h and .c files are used in compiling the program. This program results in multiple BMP files that have logic changes to the BYU Football Stadium photo. These changes are interpretted and handled differently to produce different results. (B G R Mask, Gray Mask, OR Filter)

 

### *Usage Instructions*

 

Pay close attention to the bitmap struct. The bitmap struct holds all the particular variable values you would want to use in the creation of your functions. Also, remember that when iterating through each color of a pixel, the array is one long list. This is important when dealing with special cases like the top and bottom row. Removing the color channels for a mask requires you to manipulate the value of each blue, green, and red pixel respectively. For the gray mask, either store each value to be changed later or iterate through and change each along the way. Remember for the OR filter to check the pixel above and below to bitmask the value. This ensures that each pixel is accounted for. Explain why the OR works and keep the pixel data copy and original data separate to avoid an infinite loop.

 

#### *Change Log 🚀*



## **Lab 11 Doorbell**

 

### **Description**

 

Image is the final lab in the starter folder before any major implementations of the doorbell. Learn how to manipulate bytes in C to modify image files using BMP. Enum and structs are introduced and used commonly in controlling the aspects of an image. Multiple .h and .c files are used in compiling the program. This program results in multiple BMP files that have logic changes to the BYU Football Stadium photo. These changes are interpretted and handled differently to produce different results. (B G R Mask, Gray Mask, OR Filter)

 

### *Usage Instructions*

 

Pay close attention to the bitmap struct. The bitmap struct holds all the particular variable values you would want to use in the creation of your functions. Also, remember that when iterating through each color of a pixel, the array is one long list. This is important when dealing with special cases like the top and bottom row. Removing the color channels for a mask requires you to manipulate the value of each blue, green, and red pixel respectively. For the gray mask, either store each value to be changed later or iterate through and change each along the way. Remember for the OR filter to check the pixel above and below to bitmask the value. This ensures that each pixel is accounted for. Explain why the OR works and keep the pixel data copy and original data separate to avoid an infinite loop.

 

#### *Change Log 🚀*








































































# ECEn 225 Doorbell Starter Kit

Author: <!-- Put your name here -->

Last Updated: <!-- Put a date here -->

<!-- STUDENT INSTRUCTIONS:
You will fill out this README with your project updates as you commit and push code. This README file should only be edited on your raspberry pi. Additionally, you will need to push your code back to Github after you finish each lab, so that you can create a working tree of all your changes. If you don't know how mange Github commits and pushing files to the cloud, see the instructions on the Github Setup Page: https://byu-cpe.github.io/ecen224/lab-setup/
Remember to check that your finished product compiles well in Markdown! Use this Markdown preview site: https://markdownlivepreview.com/ if you want an easy way to check.
REMOVE THIS BEFORE SUBMISSION. YOUR DOCUMENT SHOULD JUST BE YOUR WORDS -->

## Description

<!-- This should be an overview of what the project goal is, along with a sentence about where it is in its current state. -->

## Usage Instructions

<!-- This should contain all the instructions needed to access the lab, compile it from source, and run the doorbell. These should be written with the actual commands contained in `` marks (example `sudo ./main` runs the program). If you'd like, include extra details like how to customize certain features or what materials you need to build a doorbell. -->

## Updates & Changelog

<!--

This should contain a list of what features you added along with the dates. Here is a short example using a fictitious project:

### 07/13/25

- added software support for Linux
- bug fixes
- increased font size

### 07/30/25

- finalized new "about me" tab
- fixed an issue where the program crashed when run at night
- added additional settings

-->
