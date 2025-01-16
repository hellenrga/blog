+++
date = '2025-01-14T18:18:13-03:00'
draft = false
title = 'Protocols (TCP, UDP, FTP, SFTP, TFTP)'
tags = ['DevOps', 'Roadmap', 'Network']
+++

## File and Transmission Protocols

### TCP (Transmission Control Protocol)

TCP a core protocol of TCP/IP suite, used for reliable communication between devices. It's a connection oriented protocol. So, before data transmission begins, a connection is established through a three-way handshake, the image below shows it.

![three-way handshake](/images/three-way-handshake.png)  

TCP ensures data integrity by retransmitting lost packets, ordering packets, and confirming successful delivery.

Ideal for applications where accuracy and reliability are critical, such as web browsing (HTTP/HTTPS), email (SMTP/IMAP/POP3) and file transfer (FTP/SFTP).

### UDP (User Datagram Protocol)

An alternative to TCP, used for faster communication. It is a connectionless protocol, so it has no formal connection setup between devices. Data is sent without guarantee of delivery. It is faster than TCP, is suitable for time-sensitive applications like video streaming, online gaming, and DNS lookups. The thing is, there ir no error-checking or retransmission, which can result in packet loss and poor security.

## FTP, SFTP, TFTP

### FTP (File Transfer Protocol)

The standard protocol that is used to transfer files between computers and servers over a network. It is the language that computers use to transfer files over a TCP/IP network

Support file upload and download, allows directory navigation and file management on the server. But very vulnerable to interception, for exemple, data is transmitted in plaintext, including username and passwords. 

It’s suitable for non-sensitive file transfers where security is not a concern.

### SFTP (Secure File Transfer Protocol)

A secure version of FTP, it adds a layer of security by using SSH (Secure Shell) encrypting the data.

SFTP ensures confidentiality by encrypting files and credentials. Uses a single conection, simplifying firewall configurations.

It’s suitable for secure file transfers in corporate environments and over the internet.

### TFTP (Trivial File Transfer Protocol)

A simplified file transfer protocol designed for minimal functionality.

It is a connectionless (uses UDP instead of TCP) and very poorly secure protocol. There is no authentication or advanced features like directory navigation. Not recommended for sensitive data transfer.

It’s suitable for LAN (Local Area Network) environments where security and reliability are less critical. Commonly used for transferring configuration files, firmware updates or boot files in embedded systems and network devices.

| **Feature**   	| **FTP**              	| **SFTP**              	| **TFTP**                	|
|--------------------|--------------------------|---------------------------|-----------------------------|
| **Protocol**   	| TCP                 	| TCP                   	| UDP                     	|
| **Security**   	| No encryption       	| Encrypted (SSH-based) 	| No encryption           	|
| **Use Case**   	| General file transfers  | Secure file transfers 	| Local and simple transfers  |
| **Authentication** | Yes                 	| Yes                   	| No                      	|
| **Reliability**	| High                	| High                  	| Low                     	|


