# AWS Security Group Policies

**1. Do security groups support both "allow" and "deny" rules? Explain how they handle traffic filtering.**
No, security groups only support "allow" rules. You cannot create a rule to explicitly deny access. Traffic filtering operates on a default-deny basis�any traffic that does not match an explicit allow rule is automatically denied. Furthermore, security groups are stateful; if you send a request from your instance, the response traffic for that request is automatically allowed to flow in regardless of inbound security group rules.

**2. Describe what happens to all inbound traffic by default, and explain what happens to all outbound traffic by default if left unrestricted.**
- **Inbound Traffic:** By default, all inbound traffic to an EC2 instance is completely blocked (denied). You must create explicit rules to allow inbound connections.
- **Outbound Traffic:** By default, all outbound traffic from an EC2 instance is allowed unless you explicitly restrict it.

**3. Are EC2 instances internally aware of the security groups applied to them, or are they applied externally? Can one security group be reused across multiple instances?**
EC2 instances are completely unaware of the security groups applied to them. The traffic filtering is handled externally by the underlying AWS hypervisor at the Elastic Network Interface (ENI) level. 
Yes, a single security group can be applied to and reused across multiple EC2 instances, making it easy to apply consistent firewall rules across a fleet of servers.

| Port Number | Protocol Name | Purpose / Description |
| :--- | :--- | :--- |
| **22** | SSH (Secure Shell) | Secure remote command-line administration, typically used for Linux instances. |
| **21** | FTP (File Transfer Protocol) | Unencrypted transfer of computer files between a client and server on a network. |
| **80** | HTTP (Hypertext Transfer Protocol) | Unencrypted web traffic used for transmitting standard web pages. |
| **443** | HTTPS (HTTP Secure) | Encrypted web traffic used for transmitting secure web pages over TLS/SSL. |
| **3389** | RDP (Remote Desktop Protocol) | Remote administration with a graphical user interface, typically for Windows instances. |
