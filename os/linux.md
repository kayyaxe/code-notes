# Linux

# Part 1: Introduction to Linux

Linux is a free and open-source operating system kernel that forms the basis of many modern operating systems.

## Advantages/Disadvantages

| +  | - | Usages |
| --- | --- | --- |
| Customisable | Software compatibility | Developers( wide range of lib/frameworks) |
| Stable | Gamming support  | Server( Stable , Secure) |
| Secure |  | Embedded systems |
| Scalable |  | IOT |

## Core Concepts

- **Terminal:** The command-line interface where you type commands
- **Shell:** Command interpreter (usually Bash) that processes your commands
- **Root User:** Administrator account with full system access
- **Package Manager:** Tool for installing and managing software

## Essential Commands for Beginners

[**Here’s a good guide!**](Linux%201c24768679cb80ffb895c10b93e03e54.md)

```bash
ls      # List files and directories
cd      # Change directory
pwd     # Show current directory

mkdir   # Create directory
rm      # Remove files
cp      # Copy files
mv      # Move/rename files
sudo    # Run command as administrator

touch   # Make new file
nano    # Edit file content
cat     # Display file content
```

## File System Basics

![image.png](Linux%201c24768679cb80ffb895c10b93e03e54/image.png)

## Linux Distributions

A Linux distribution (or "distro") is an operating system built on top of the Linux kernel. Each distribution packages the kernel with different software, tools, and user interfaces.

### Ubuntu

Ubuntu is one of the most popular Linux distributions, especially for beginners. It features:

- **User-friendly interface:** Uses GNOME desktop environment by default
- **Large community:** Extensive support forums and documentation
- **Regular updates:** New versions released every 6 months, with Long Term Support (LTS) versions every 2 years
- **Package management:** Uses APT (Advanced Package Tool) with access to thousands of software packages

Ubuntu serves as both a desktop and server operating system, making it versatile for different use cases.

### Other Popular Distributions

- **Fedora:** Cutting-edge features, sponsored by Red Hat
- **Debian:** Known for stability, Ubuntu's parent distribution
- **Linux Mint:** Based on Ubuntu, focuses on out-of-the-box usability
- **CentOS:** Enterprise-focused, popular for servers

### FYI

## Security and Permissions

Linux is known for its robust security model and file permission system.

- **User Types:** Regular users, system users, and root (superuser)
- **File Permissions:** Read, Write, Execute (rwx) for Owner, Group, and Others
- **SELinux:** Security enhancement providing mandatory access control

## System Services and Daemons

Services that run in the background to handle various system tasks:

- **systemd:** Modern init system and service manager
- **cron:** Job scheduler for automated tasks
- **sshd:** Secure Shell daemon for remote access
- **networking:** Network configuration and connectivity

## Shell Scripting

Automation and system administration through shell scripts:

- **Bash:** Most common shell, powerful scripting capabilities
- **Variables:** Store and manipulate data
- **Control Structures:** if/else, loops, case statements
- **Functions:** Reusable code blocks for complex tasks

## Linux Networking

Essential networking concepts and tools:

- **TCP/IP:** Primary networking protocol suite
- **Network Configuration:** IP addressing, routing, DNS
- **Common Tools:** ping, netstat, curl, wget, ssh
- **Firewall:** iptables/nftables for network security

# Part 2: Linux Interview Preparation

## Key Interview Topics

1. Process Management- What is a process?
  Answer: A process is an instance of a running program with its own memory space and resources.

- Difference between process and thread?
  Answer: Processes are independent and have separate memory spaces, while threads share memory within the same process.

- How to view running processes?
  Answer: Using commands like ps, top, or htop
2. File System- What is an inode?
  Answer: A data structure that stores metadata about files (permissions, size, location).

- Explain file permissions?
  Answer: Read (r), Write (w), Execute (x) permissions for User, Group, and Others.

- What are hard links vs soft links?
  Answer: Hard links share the same inode, soft links are like shortcuts pointing to the original file.
3. Memory Management- What is virtual memory?
  Answer: A memory management technique that uses disk space to extend RAM.

- Explain swap space?
  Answer: Disk space used as virtual memory when physical RAM is full.

- How to check memory usage?
  Answer: Using commands like free, top, or vmstat
4. Common Troubleshooting Scenarios- High CPU usage:
  1. Check top/htop
  2. Identify resource-heavy processes
  3. Review system logs

- Disk space issues:
  1. Use df -h to check space
  2. Find large files with du
  3. Clear temporary files/logs

- Network connectivity:
  1. ping for basic connectivity
  2. netstat for port status
  3. traceroute for path tracing