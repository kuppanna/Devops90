# Core Components of Linux
# 1 Kernel

The kernel is the core of the Linux operating system. It:

Manages CPU, memory, and devices

Handles process scheduling

Controls hardware communication

Manages filesystems and networking

It acts as a bridge between hardware and software.

# 2 User Space

User space is where user applications run.
Examples:

Shell (bash)

Web servers

Databases

Python programs

Applications in user space do not directly access hardware — they communicate with the kernel using system calls.

# 3 Init / systemd

The first process started by the kernel is PID 1, traditionally called init.

Modern Linux distributions use systemd instead of traditional init systems.

It is responsible for:

Booting the system

Starting services

Managing background processes

Handling system shutdown

# 4 How Processes Are Created and Managed
 Process Creation

In Linux, a process is created using:

fork() → Creates a copy of the parent process

exec() → Replaces the process memory with a new program

Example flow:

You run ls

The shell calls fork()

The child process calls exec()

The kernel schedules it for execution

# 5 Process Management

The kernel:

Assigns a unique PID (Process ID)

Schedules CPU time

Tracks memory usage

Handles signals (SIGTERM, SIGKILL)

Manages process states (Running, Sleeping, Zombie)

Useful commands:

ps

top

htop

kill

# 6 What systemd Does and Why It Matters

systemd is a modern init system that:

 Starts Services in Parallel

Faster boot time compared to older init systems.

 Manages Services (Daemons)

You can:

systemctl start nginx
systemctl stop docker
systemctl status sshd
 Handles:

Logging (journald)

Mount points

Timers (cron alternative)

Service dependencies

# 7 Why It Matters

Centralized service management

Faster system startup

Automatic service restart

Dependency handling

Standard across most modern Linux distributions

Without systemd, services would not automatically start, stop, or restart properly.