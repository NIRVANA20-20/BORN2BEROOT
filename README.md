               This project has been created as part of the 42 curriculum by <olaizi>

# BORN2BEROOT

## Description:

Born2beroot is a project about setting up a secure Linux virtual machine
You learn how to manage users, permission, sudo, SSH, and the firewall
the goal is to understand basic Linux system administration and security

### Virtual Machine:

A virtual machine is a software-based computer that runs inside a real computer.
It uses the real machine's resourcse (CPU, memory, disk) but works like a separate system
Each virtual machine has its own operating system and is isolated from the main system
which makes it safe for testing, learning, and system cofiguration

**Virtualization:**

Virtualisation lets one real computer run many virtual computers at the same time using a ***Hypervisor***.
Each virtual computer works like a real computer but is safe and separate from the main systemi.

**VirtualBox vs UTM**

- **VirtualBox:** Cross-platform, feature-rich, widely supported.  
- **UTM:** Lightweight, optimized for macOS and ARM, easy to use, fewer features.


**Hypervisor:**

A hypervisor is software that lets a computer run multiple virtual machines at the same time
shares CPU, memory, and storage, keeping each virtual machine separate and safe.
There are two main types:

Type 1 (Bare-metal) – Runs directly on the computer’s hardware. Example: VMware ESXi, Microsoft Hyper-V.
Type 2 (Hosted) – Runs on top of an existing operating system. Example: VirtualBox, VMware Workstation.

## Operating System:

We used **Debian** because it is stable and easy to learn. **Rocky Linux** is also an option for more advanced users.  

- Debian: easy, stable, big community.  
- Rocky Linux: enterprise, stable, uses SELinux.  

## Disk Partitions:

In this project, we use **LVM** (Logical Volume Manager) to organize the disk. We create separate partitions for better management and security:

- **`/` (root):** Main system files.  
- **`/home`:** User files, so personal data is separated.  
- **`/var`:** Logs and variable data.  
- **`/tmp`:** Temporary files. 

## Security Policies:

AppArmor enabled to restrict application behavior.

### AppArmor:

AppArmor is a Linux kernel security module that allows administrators to restrict the capabilities of programs through per-program profiles.
Profiles define what a program is allowed to do, such as accessing certain files or using network resources, providing an extra layer of mandatory access control to supplement standard Linux permissions

**AppArmor vs SELinux**

- **AppArmor:** Path-based, easier to configure, suitable for beginners.  
- **SELinux:** Label-based, more granular and powerful, steeper learning curve.

## User Management:

Root user secured, standard users created with limited privileges, password policies enforced.
The user is added to the sudo group to run admin commands safely..

**Root**

The root directory serves as the foundation of the filesystem, while the root user holds the highest administrative privileges.

**SUDO**

The sudo (short for Superuser Do) command is one of the most important commands in Linux. It's a prefix you add to other commands to run them with the administrative privileges of another user (by default, the root user).

## Services Installed:

SSH for remote access, firewall for network protection, essential system utilities.

**SSH (Secure shell)**

The Secure Shell Protocol (SSH Protocol) is a cryptographic network protocol for operating network services securely over an unsecured network. Its most notable applications are remote login and command-line execution.

**UFW (Uncomplicated Firewall)**

UFW (uncomplicated firewall) is a command-line tool designed to simplify firewall management on Linux systems Built on top of iptables, it provides a user-friendly way to define rules for controlling network traffic, such as allowing or blocking specific ports, IP addresses, or services.

- UFW: Simple, ideal for Debian-based systems.  
- firewalld: Dynamic firewall management, more features, common in Red Hat-based systems.

**PAM (Pluggable Authentication Modules)**

Linux PAM helps by providing a flexible way to manage user authentication and security.

## Resources

The following resources were used to understand and complete the Born2beRoot project:

### Documentation & Articles

- SSH (remote access):  
  https://www.redhat.com/en/blog/access-remote-systems-ssh

- Sudo command:  
  https://www.geeksforgeeks.org/linux-unix/sudo-command-in-linux-with-examples/

- Firewall basics:  
  https://www.geeksforgeeks.org/computer-networks/introduction-of-firewall-in-computer-network/

- PAM (Pluggable Authentication Modules):  
  https://www.geeksforgeeks.org/linux-unix/what-is-linux-pam-module-and-how-to-configure-it/

- Bash scripting:  
  https://www.gnu.org/software/bash/manual/bash.html

- Born2beRoot subject explanation:  
  https://noreply.gitbook.io/born2beroot

### AI Usage

AI tools were used as a **learning assistant** during this project.

AI was used for:
- Explaining Linux concepts such as **LVM**, **AppArmor**, **sudo**, and **SSH**.
- Helping understand Bash scripting logic.
- Assisting in writing and simplifying the README documentation.
- Clarifying errors and command behavior.
- Help understand **LVM concepts**.
- Help explain **AppArmor security profiles**.
