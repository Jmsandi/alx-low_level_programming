# Project README

## Introduction
This project aims to provide a comprehensive understanding of file handling and I/O system calls in programming. It covers topics such as creating, opening, closing, reading, and writing files, file descriptors, standard file descriptors, flags, file permissions, system calls, and the difference between functions and system calls.

## Table of Contents
- [File Handling](#file-handling)
  - [Creating Files](#creating-files)
  - [Opening Files](#opening-files)
  - [Closing Files](#closing-files)
  - [Reading Files](#reading-files)
  - [Writing to Files](#writing-to-files)
- [File Descriptors](#file-descriptors)
- [Standard File Descriptors](#standard-file-descriptors)
- [POSIX Names](#posix-names)
- [Flags](#flags)
- [File Permissions](#file-permissions)
- [System Calls](#system-calls)
- [Functions vs System Calls](#functions-vs-system-calls)

## File Handling

### Creating Files
When working with files, one of the first steps is creating a file. In most programming languages, you can create a file using system calls or built-in functions provided by the language's standard library. The specific method may vary depending on the programming language or operating system being used.

### Opening Files
To work with an existing file, you need to open it. Opening a file typically involves associating a file descriptor with the file, which allows subsequent operations on the file. The `open` system call is commonly used for this purpose.

### Closing Files
After you finish working with a file, it is essential to close it properly. Closing a file releases the associated file descriptor and frees system resources. In programming languages, there are typically functions or system calls like `close` to close an open file.

### Reading Files
Reading from files allows you to retrieve data stored within them. Depending on the programming language and system calls used, you can read files in different ways, such as reading a single character at a time or reading an entire line or block of data.

### Writing to Files
Writing to files enables you to store data in them. Similar to reading files, there are various methods to write data, such as writing a single character, writing a string, or writing a block of data.

## File Descriptors
In many operating systems, file descriptors are used to represent opened files. A file descriptor is an abstract indicator used by the operating system to access a file. It serves as a communication channel between the process and the operating system's file system.

## Standard File Descriptors
There are three standard file descriptors available to a process by default:

1. **Standard Input (stdin)**: This file descriptor represents the standard input stream. It is typically associated with the keyboard or input device. In POSIX systems, its file descriptor number is 0.

2. **Standard Output (stdout)**: This file descriptor represents the standard output stream. It is used for normal output operations. In POSIX systems, its file descriptor number is 1.

3. **Standard Error (stderr)**: This file descriptor represents the standard error stream. It is used for error or diagnostic output. In POSIX systems, its file descriptor number is 2.

## POSIX Names
The POSIX names for the standard file descriptors are as follows:

- Standard Input: STDIN_FILENO
- Standard Output: STDOUT_FILENO
- Standard Error: STDERR_FILENO

## Flags
When opening files using the `open` system call, you can provide flags to control the file's behavior. Some common flags include:

- `O_RDONLY`: Opens the file for reading only.
- `O_WRONLY`: Opens the file for writing only.
- `O_RDWR`: Opens the file for both reading and writing.

These flags determine the access mode of the opened file.

## File Permissions
File permissions control who can access a file and what operations they can perform on it. When creating a file using the `open` system call, you can specify the permissions using an octal value. The permissions include read, write, and execute permissions for the owner, group, and others.

## System Calls
A system call is a mechanism provided by the operating system that allows user-level processes to request services from the kernel. System calls provide an interface for interacting with the underlying operating system, such as file I/O, process management, network communication, etc. Examples of system calls include `open`, `close`, `read`, and `write`.

## Functions vs System Calls
In programming, functions and system calls serve different purposes:

- **Functions** are blocks of reusable code within a program or library. They are typically written in the same programming language as the rest of the code and are used to encapsulate a specific behavior or logic.

- **System calls**, on the other hand, are requests made by user-level processes to the operating system kernel for specific services or operations. System calls involve transitioning from user mode to kernel mode, where the requested operation is performed. System calls often provide low-level access to resources, such as files, devices, or network sockets, that are managed by the operating system.

While functions are typically executed within the user's address space, system calls involve a context switch from user mode to kernel mode to access privileged resources and perform operations that cannot be done directly within the user space.

## Conclusion
This project provides an overview of file handling, file descriptors, standard file descriptors, flags, file permissions, system calls, and the distinction between functions and system calls. Understanding these concepts is essential for effective file manipulation and I/O operations in various programming languages and operating systems.
