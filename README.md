# My OS project

The purpose of this project is to learn about the basic operating systems concepts by attempting to create an operating system of my own.

### Main objectives

The end goal is to create an operating system that, from the end user's perspective, launches a shell with which simple programs can be executed : ```echo```, ```top```, ```ps```, ```kill```


From there we can then work on expanding the operating system's capabilities by going in one of the following directions

### Secondary objectives

- File system

Create a directory structure and the ability to create and write to files (for now we can just use ```echo``` and redirect output to the file) : ```mkdir```,```rmdir```,```touch```,```rm```,```cat```, ```ls```

- Games

This entails writing simple userland games that the user can run just as she would a typical shell command : snake, space invaders, etc.

- Portability

This requires figuring out what we need to do to be able to run external C programs. We will need to investigate how to write a minimalistic C library and make it available to those programs. Perhaps we could port an existing C library itself.

- Text editor

We could implenent something minimalistic that allows us to edit files. Think Vim.

### Milestones

In order to pursue this project we need to start by defining some milestones we want to hit.

- Phase 1 : setup environment

Make decisions on the general tool chain to be used.

- Phase 2 : writing the bootloader

Research what the boot code is supposed to do and how to write it.

Key words include : bootloader, assembly, system memory layout

- Phase 3 : getting to main.c

Jump to the starting C code from the bootloader and figure out what kind of setup needs to be done in this initialization function.

Key words include : interrupts, processes, memory management.

- Phase 4 : printing to the console

Start writing a small C library to be used by the kernel and which can initially implement the printf function.

Key words include : video memory

- Phase 5 : planning the memory map

Research virtual memory VS physical memory, how to setup the memory manager and the memory layout.

Key words include : virtual memory manager, physical memory, virtual memory

- Phase 6 : implementing processes

Research what needs to be done in order to run a very simple compiled program which for example returns a constant number.

From this research I can start figuring out how to design the structure of processes, how to allocate memory for them, how to get them to run and how to schedule them.

Implement fork(), kill(), waitpid() so that processes can interact with each other.

Research IPC.

- Phase 7 : implement the shell process

Enable keyboard support.

Implement a shell.
