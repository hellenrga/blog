+++
date = '2025-01-03T17:10:38-03:00'
draft = false
title = 'Docker, Linux Server, Shell Scripting.'
tags = ["Linux", "Docker", "AWS", "DevOps"]
+++

# Diving into DevOps

I already have a solid foundation in DevOps tools through my professional experience and studies, I believe there’s always room to deepen my understanding. To strengthen my knowledge further, I decided to revisit the basics and embark on a Starter DevOps course offered by Alura, one of Brazil’s premier tech education platforms.

This course spanned 32 hours and was divided into three modules: **Linux CLI, Secure Traffic, and Docker.** Each module built upon the fundamentals and provided hands-on experience, ensuring a well-rounded grasp of essential DevOps concepts.

Here’s the certification for completing this journey:  
![Certificate](/images/start-devops-certificate.png)

## 1 | Linux Server and CLI

Though Linux has been a familiar playground for me—it was my primary operating system for a couple of years—I had primarily used it in a desktop environment. But at some point I eventually switched back to other OSs because it didn't have support for games (😅) but I still continued playing around with Linux through virtual machines for coding.

This course introduced me to **Linux Server**, which was a new challenge. Using **SSH connections**, I set up and managed a server, gaining hands-on experience with server environments.  

One of the most fascinating aspects was learning **Shell Scripting** for task automation. I wrote scripts to:  
- **Back up files**,  
- **Compress and decompress data**,  
- **Convert images from JPG to PNG**, and more.  

These scripts were a gateway to understanding how automation streamlines workflows. I’ve uploaded them to my **Homelab repository**—feel free to explore it [here](https://github.com/hellenrga/homelab).

![Linux Server](/images/start-linux-server.png)

## 2 | Web Communication and Security

Although I already had a strong understanding of the fundamentals of web communications from my college studies, I found it valuable to revisit and deepen my knowledge of HTTP protocols and associated tools. I had the opportunity to explore a variety of essential topics and hands-on practices that enhanced my skillset.

### Key Learning Outcomes

- **Postman Usage**: Gained practical experience using **Postman** to debug HTTP requests, configure headers, and test authentication methods, enhancing my understanding of secure communication.

- **Session & Cookie Management**: Implemented **cookies** and **sessions** to maintain user identity across requests, reinforcing knowledge of stateful web communication.

- **OpenSSL & Encryption**: Explored **OpenSSL** for encryption and delved into **SSL/TLS layers** to secure data transmission and protect client-server communication.

- **Networking Protocols**: Revisited **UDP** and **TCP** protocols for reliable data transmission, and learned about **QUIC** as part of the next-gen **HTTP/3** for better performance and security.

## 3 | Docker

I had minimal prior experience with Docker, and this course allowed me to deepen my understanding of containerization and orchestration. After gaining a foundational understanding of what Docker is and how it works, I started creating containers, interacting with them, and managing images. I worked with Docker commands to run web applications within containers.

I used the following command to run an application in the background, exposing all available ports:

```bash
docker run -d -P docker/example
```

Additionally, I specified the ports to open for access to the application using the following command:

```bash
docker run -d -p docker/example 3000:80
```

For example, I was able to run a web application on port 8080 and access it locally.

![image](/images/localhost-site.png)

I also learned to manage Docker processes, such as stopping running containers:

```bash
docker stop $(docker ps -q)
```

Moreover, I learned how to create Docker images using the following command:

```bash
docker build -t <tag>
```

In addition to these basic Docker operations, I explored mechanisms for data persistence, such as **volumes**, **bind mounts**, and **tmpfs**. These methods help ensure that data is stored securely and persists across container restarts.

Example of using **tmpfs** for temporary storage:

```bash
docker run -it --mount type=tmpfs,target=/tmp ubuntu
```

![image](/images/using-tmpfs.png)

### Building a DevOps Mindset  

This initial phase of my DevOps learning journey has not only expanded my technical toolkit but has also deepened my understanding of how modern infrastructures operate. I’m excited to continue exploring Docker, Kubernetes, and beyond, as I pursue a future in cloud-native technologies and scalable systems.

Next, I'll be diving into Kubernetes and exploring advanced container orchestration. Stay tuned for more!
