![Awesome Creative Portfolio Websites](my-portfolio-1-638.jpg)

## Important Terms and References
### Terms

- **Black-Box Penetration**: Testers are expected to attack the target as an outsider with no previous knowledge of the environment.
    > **Example**: Here testers are paid to learn as much as they can about the environment and it's vulnerabilities, from an outside perspective.

- **White-Box Penetration**: Testers have full knowledge of the environment allowing them to tear apart subtle security issues.
  > **Example**: This is most appropriate when the client wants a detailed analysis of all potential security flaws.

- **Pentesting Execution Standard (PTES)**: An industry standard framework for penetration testing.
  > **Example**: Steps for the PTES include:
      - Pre-engagement interaction
      - Intelligence gathering / mapping
      - Threat modeling
      - Vulnerability assessment
      - Exploitation
      - Post-exploitation
      - Reporting

- **Banner Grabbing**: entails opening a connection to a port and printing out anything that the servers sends within 5 seconds.
  > **Example**: Banner Grabbing is used to quickly determine what OS and services are being offered by a target.

- **Black-Box Penetration**: Definition
  > **Example**: Example usage here

- **ShellShock**: A bash exploit that allows an attacker to execute Bash commands with HTTP requests.

- **Common Gateway Interface (CGI)**: There are many ways to serve websites. One is called **CGI (Common Gateway Interface)**,  which defines a **standard**, or set of rules, that allows clients to run scripts on a server.
  > **Example**: A bug in CGI is what allows the ShellShock exploit to work.

- **BurpSuite**: A software suite that specializes in web vulnerability exploitation.

- **MSFconsole** is used for the reconnaissance, vulnerability analysis, and exploitation phases of a penetration test.
  > **Example**: MSFConsole uses 4 different types of modules:

    - **Auxiliary modules** are used for information gathering, enumeration, port scanning, and that sort of thing. There are plenty of useful tools in there too for things like connecting to SQL databases and even tools for performing man-in-the-middle attacks.

    - **Exploit modules** are generally used to deliver exploit code to a target system. You can also perform a search for modules using the search command.

    - **Post modules** offer post exploitation tools such as the ability to extract password hashes and access tokens and even modules for things like taking a screenshot, key-logging, and downloading files. You'll explore these during the next class.

    - **Payload modules** are used to create malicious payloads to use with an exploit. If possible, the aim would be to upload a copy of Meterpreter, which is the default payload of Metasploit.

- **Meterpreter** is a post-exploitation tool used to interact with compromised targets. Metasploit loads this automatically if an exploit is successful.


## References

  - [Official NMap Tutorial](https://nmap.org/book/port-scanning.html)
  - [Metasploit Databases](https://www.offensive-security.com/metasploit-unleashed/using-databases/)
  - [Hydra Github](https://github.com/vanhauser-thc/thc-hydra)

- **Host Discovery**: The process of discovering live hosts on a network.
  > **Example**: One way to do this is ping every IP address in the, subnet and see which ones respond. This is important because it enables attackers to identify potential targets.

- **Service Discovery**: The process of discovering which services are running on a reachable host.
  > **Example**: The first step is typically a port scan, which reveals which ports are open on a machine.

- **Passive OS Detection**: nmap guesses which operating system is running on the target of a port scan by looking for clues in a machine's responses.
  > **Example**: A TCP response generated by a Windows machine will contain the same raw data as one generated by a Linux machine, but the Time to Live will often be different: Windows sets it to 128 by default, while Linux has 64.

- **Active OS Detection**: More accurate than nmap's passive detection, but also more invasive and more likely to be identified.
  > **Example**: You should only use Active OS Detection on one host at a time.

- **Brute Force Attack**: Also known as a 'dictionary attack' An attacker uses a list of passwords to try to log in as a given user.
  > **Example**: An attacker might try to log in as the user admin with the passwords password; administrator; 12345; etc, hoping that one of them will work.

- **Pillaging** the act of exfiltrating valuable data from a compromised host. This is the phase during which you collect sensitive information about your target.
- **Fuzzing**: The act of sending fake data in order to "trick" the service into behaving a certain way. A brute-force attack against an SSH server using the `ssh_login` module is a good example.

- Metasploit has modules for three different kinds of scanning:
  - **Port Scans**: Metasploit can perform TCP connect and SYN scans.
  - **Service Scans**: Metasploit has a wealth of modules for scanning specific services. These modules are useful for detecting the version of a specific service.
  They can also be used for more advanced purposes, such as "fuzzing" the target service.
  - **Post-Exploitation Enumerations**: Scans that are run on compromised hosts after you've hacked into them. These can be used to scan for information like a list of installed applications, users, running processes/services, and/or stored credentials.

- **Post-exploitation** is the most complicated phase of a pentest, because there are so many things an attacker might try to do. Some common examples include:

- **Gather data about the compromised host**. One of the first things attackers do after compromising a host is learn as much as they can about it.

**Enumeration** is the process of of learning as much as you can about a victim machine, often from system and configuration files. Metasploit provides a wealth of modules specifically for post-exploitation data enumeration.

- **Maintain Access**. If you exploit a host and lose your connection, the only way to get it back is to exploit it again. To avoid this, attackers often leave "backdoors" on compromised targets.

- **Steal data**. Stealing data is commonly called **data exfiltration** or **pillaging**.    
  > **Example**: In addition to the information above, attackers will look for client-specific data, such as financial records; business documents; confidental communications; etc.

- **Pivot**. Pentesters often manage to compromise machines that have multiple network interfaces. Each network interface attached to a machine allows it to communicate with a different subnet. This means that compromising a machine with multiple network interfaces might allow attackers to _pivot_ into completely new networks. This sometimes results in their compromising machines on sensitive internal networks that were assumed to be safe, which can have disastrous consequences: Exfiltration of employee PII, confidential financial records, executive correspondences, etc.


- **Pivot**: Pivoting is act of routing data _through_ a _pivot point_ in order to communicate with a target network.
  >**Example**: You can pivot to machines on subnets by **routing** through a host that _does_ have an interface, such as a router.

- **DMZ**: The `Demilitarized Zone` is a network that sits in-between the internet and the internal network of an organization. All interenet traffic must pass through the `DMZ` before being routed into the network.
  >**Example**: While DMZs add an extra layer of protection to a network, they are not impenetrable. Attackers can still exploit machines on the internal network by compromising a machine in the DMZ and using _it_ to send traffic to the intranet.

- **System privileges** are typically called **root privileges** on Linux.
  > **Example**: A **system shell**, or **root shell**, is one that runs with system privileges.

- **User Privileges**: Applications like Firefox and MS Word run with user privileges.
  > **Example**: By default, users only have privileges to modify files they own. They cannot make changes to other users' environments.

- **Administrator**: Administrators can modify anyone's files and application configurations, and have full privileges to reconfigure the system.
  > **Example**: Typically, gaining administrator privileges to a system is one of the first things an attacker tries to do.

- **Escalate Privileges**: This is the act of gaining administrator privledges on a compromised target.
  > **Example**: Once a system has been breached, an attacker attempts to escalate privileges so they have full control over the system.

- **SYSTEM**: When the WIndows OS runs a service that needs elevated privileges, it will run with `SYSTEM` privileges.
  > **Example**: `SYSTEM` privileges are identical to Administrator privileges in scope, but `SYSTEM` privileges are used only by the operating system, _not_ by user accounts.

- **Named Pipe**: "Pipes" in Windows are conceptually similar to those in Linux: They are simply a stream of data. Programs can use pipes to send data back and forth.
  >**Example**: A "named pipe" allows a running process to pass data to another. The process sending data is called a **pipe server**, and the recipient is called a **pipe client**.

- **Named Pipe Impersonation**: This is a Windows feature that enables a pipe _client_ to run commands with the same privileges as the pipe _server_.
  >**Example**: "Named pipes" allow a process to run with elevated privileges. If the pipe server has administrative privileges, _this means that a pipe client with user privileges can use named pipe impersonation to run commands with administrative privileges_.

- **Tokens** are pieces of data that systems use to authenticate users. On Windows, **Kerberos** is the most common token authentication protocol.
  >**Example**: When a user logs in, they are issued a unique token. They then pass this token along with future requests to prove their identity.

- **Token Duplication**: Metasploit is able to duplicate and re-use existing user tokens, allowing you to impersonate other authenticated users.
  > **Example**: Token duplication allows access to systems by using tokens that have been generated by other users.

- **NetBIOS**: A particular network transport that is part of the LAN Manager protocol suite. NetBIOS uses a broadcast communication style that was applicable to early segmented local area networks.
  >**Example**: A protocol family including name resolution, datagram, and connection services.
