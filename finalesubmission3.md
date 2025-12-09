# **ECEn 225 🖥️ Doorbell Starter Kit 6\-11 Finale**

Author: Cael Dearden

Last Updated: December 8th, 2025

 

## **Table of Contents 📚**

1. [Display](#lab-06-display)

2. [File](#lab-07-file)

3. [Camera](#lab-08-camera)

4. [Client](#lab-09-client)

5. [Threaded Client](#lab-10-threaded-client)

6. [Doorbell](#lab-11-doorbell)

 

 

## **About 💭**



As this marks the end of the semester, the purpose of the ECEn 225 Doorbell Lab Finale is to implement code that makes a fully functional smart doorbell. Through this README I will teach you what we have done in each lab, explain the necessary descriptions of each lab, and include the usage instructions to replicate the project. This README file is also a show of our knowledge to create and show our abilities of industry-standard techniques. A README follows *markdown* formatting and convention. I will now go through five labs explaining the flow and timeline of the doorbell project. It is also important to note that there will be a changelog to combat technical debt along the way.

 

## **Lab 06 Display**

 

### **Description**



Covering the LCD display and buttons for the Pi Z2W in the ECEn 225 lab kit. For the first time we also get to experience a Makefile. After basics of the LCD, we focus on using graphical libraries to initiate certain outputs.
 
 

### *Usage Instructions*



To start off the lab, we will be using the BCM2835 library. The library includes the Makefile. The download is here [BCM2835-Download](http://www.airspayce.com/mikem/bcm2835/bcm2835-1.71.tar.gz). Using the terminal will be an easier experience. Use the `display.h` library to initialize the screen and implement the following functions to master the screen. `clearScreen` `drawHelloWorld` `drawChars` `drawStars` `drawFlag` Note that there are tools to use such as log to help test the code you make and compile.
 


#### *Change Log 🚀*

12-8-25 Nothing of importance

 

 

## **Lab 07 File**

 

### **Description**

 

Now that we have the screen initialized, we will want to read files into the program. A doorbell needs to store and call files because it is treated like an interface. After this is achieved, the files will be filtered out based on use case scenarios.

 

### *Usage Instructions*

 

Initially, we need to understand the where images get stored and that is in a folder. A directory pointer, `DIR *dp`, as example, hold information on entries in a specified directory. Opening a directory allows you to parse and read data in a folder. Specifically, we will be focusing on the `FILE` stream and the `.bmp` and `.log` files. When a file is opened, new input can be read. In this lab you want to grab entries and draw a menu with those files you have acquired. Then draw the image using a draw_file function.

 

#### *Change Log 🚀*

12-8-25 Right as rain, no changes reported to code

 

 

## **Lab 08 Camera**

 

### **Description**

 

Camera focuses on the ability to take a picture with the built-in camera doorbell. In order to do this, a buffer is initiated and the raw data is stored. We must format the data with certain file types and storage such as `malloc`. After that, the viewer interface will be updated to show the stored photo taken.
 

### *Usage Instructions*

 

Create a buffer with a known size. This buffer will use `malloc` afterwards to indicate the amount of data you actually want to receive. The buffer is then stored in the heap. Note that the heap has a finite amount of space. After this, write to a file. Make a camera_save_to_file function to initiate everything. Spacing out your code will help out in the long run. Then display the image data on the screen.

 

#### *Change Log 🚀*

11-11-25 Added a camera helper function to make my main function more concise. Watch out for technical debt when implementing new features.

 

 

 

## **Lab 09 Client**

 

### **Description**

 

For Client, we will be interacting and gaining knowledge of structs. These structs will also handle raw data in a buffer. A struct is a group of variables that relate to the same object. An example of this would be that a rectangle has a length and width that both attribute back to the rectangle. After the data is caught, it will be sent over a network socket.

 

### *Usage Instructions*

 

Understand the server that you want to ping and find the IP address. An IP address is a specific location to a domain or computer that lives in the internet. Think of them as a real address to a house or business. Ports are entry points that programs use to communicate. If a computer uses or tries to go through the wrong port in an `ssh` connection, security usually does not allow them to connect. Create a struct that uses your port, host, and homework id data. Use your camera capture function which was implemented earlier. Implement a client send image that takes your data and packages it for the client to receive the response. Make sure to close the client or else the socket can bug out.


 

#### *Change Log 🚀*

11-18-25 Implemented a Send Flick function to handle the picture data to the servers.

 

## **Lab 10 Threaded Client**

 

### **Description**

 

Here, we want to be able to send the picture data to the servers while also showing a status bar in the mean time. This requires us to use threads and multitask in C, which was previously thought as impossible. As such, we might have to go back and change some of our functions to deal with technical debt. This thread will deal with arguments and run off a global variable.
 

### *Usage Instructions*

 
Instead of a single path of execution, we will be running multiple at a time. This means we can upload a photos while drawing to the screen etc. To create a thread, use the `pthread_t` header. This header will give you all the functions and tools you need. `pthread_join()` gives you a return value from the function. We do not use it in this lab so we can ignore its use for now. Best way to implement the threaded client is make a send image function. This function will handle the logic sending it to the server. Once it is done it will update a global variable. A status bar function will then run off this global variable and change the bar status. After that, the doorbell will go back to the main menu.

 

#### *Change Log 🚀*

11-24-25 Had to make a new struct in order for the send image to not interfere with the struct of the camera helper function. Works better in the long run.



## **Lab 11 Doorbell**

 

### **Description**

 

As the last lab, we will fully integrate the doorbell personal by using daemons. A daemon is a system process that runs a service manager. It is responsible for the processes used on technology. We will use this to our advantage by managing the boot process. The program will run off of boot and deal with different levels of operation depending on the use.

 

### *Usage Instructions*

 

We will start off by understanding service files. Go in the terminal and create a file in `/etc/systemd/system`. This file will require the absolute path of the file and wherever main, where you run the program, is stored. After this, make sure the system is enabled and a doorbell.service exists. When you a sudo start command and reboot the doorbell, it will automatically run the program. Hide the file menu because we want it to look like a real doorbell. Implement a hidden way for only you to get inside such as up up down buttons pressed in succession. Make sure the people know the doorbell has been rung when it is pressed.

 

#### *Change Log 🚀*

12-8-25 Marked out a bunch of my code that was not needed. Took out the bitmasks and made sure it did not go to the draw menu prematurely.

