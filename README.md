# -Subject-Computer-Application-and-Security-Task-Part-1

# Kali Linux and Metasploitable2 Setup and Exploitation Guide

This guide provides step-by-step instructions for setting up Kali Linux and Metasploitable2, finding their IP addresses, and exploiting a known vulnerability.

## Setup Kali Linux and Metasploitable2

1. **Download and Install Kali Linux:**
   - Download the latest version of Kali Linux from the official website: [https://www.kali.org/downloads/](https://www.kali.org/downloads/)
   - Follow the installation instructions provided on the website.

2. **Download and Import Metasploitable2:**
   - Download Metasploitable2 from the following link: [https://sourceforge.net/projects/metasploitable/](https://sourceforge.net/projects/metasploitable/)
   - Import the Metasploitable2 virtual machine into your preferred virtualization software (e.g., VirtualBox, VMware).

3. **Start Kali Linux and Metasploitable2:**
   - Launch both Kali Linux and Metasploitable2 virtual machines.

## Finding IP Addresses

1. **Find IP Address of Kali Linux:**
   - Open a terminal in Kali Linux.
   - Use the `ifconfig` command to display network interfaces and their IP addresses.

2. **Find IP Address of Metasploitable2:**
   - Similarly, open a terminal in Metasploitable2.
   - Use the `ifconfig` command to find the IP address assigned to the network interface.

## Basic Commands

1. **Ping Command:**
   - In Kali Linux terminal, use the `ping` command followed by the IP address of Metasploitable2 to check network connectivity.

## Searching for Vulnerabilities

1. **Search for vsftpd 2.3.4:**
   - Use the `search` command in Metasploit framework to find modules related to vsftpd 2.3.4.
   - Example: `search vsftpd 2.3.4`

## Exploiting a Known Vulnerability

1. **Exploit vsftpd 2.3.4 Backdoor:**
   - Within Kali Linux, open a terminal and launch Metasploit framework by typing `msfconsole`.
   - Use the `use` command to select the vsftpd 2.3.4 backdoor exploit module.
   - Example: `use exploit/unix/ftp/vsftpd_234_backdoor`
   - Use the `show options` command to display available options for the exploit.
   - Set the RHOST option to the IP address of Metasploitable2 using the `set` command.
   - Example: `set RHOST <Metasploitable2_IP>`
   - Finally, execute the exploit using the `exploit` command.

## Disclaimer

This guide is for educational purposes only. Ensure that you have proper authorization before performing any security testing or exploiting vulnerabilities.
