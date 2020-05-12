---
layout: post
title: My Interview Experience
description: My interview experience during on campus placements for Directi
category1: Personal
---


<br><br>
### Media.net (Directi) Interview Experience for SRE Role | (On Campus)

Media.net came to our campus for Site Reliability Engineering role. The selection process had MCQ round followed by socket programming round and technical interview round


<br><br>
### Key to succeed:
In-Depth knowledge of Computer Networks and Operating System is required. Also, socket programming is must while knowledge of basic Linux commands is a plus.

There were two rounds before the Face to Face Technical Interview. First one was an online 45 minutes MCQ test consisting of 40 questions.

<br><br>
### Online MCQ Test:  
Questions were from Operating System, Computer Networks, Algorithms, Data Structures, DBMS, General Aptitude. 54 students were shortlisted for the next programming test.

<br><br>
### Offline Programming Test:
2nd round was a 3-4 hour offline socket-programming test. They(Directi people) gave one problem consisting of 3 sub questions and two bonus questions. Internet connection was turned off and they had setup their own Virtual Machine server. A URL was provided which contained all the information about the problem statement and FAQs. It also contained manuals for programming languages including C, C++, Java, Python (2/3), Go, etc. For socket programming, it is always better to use Python. However, other students used C, C++ and Java also. We had to write one server program and extend the codebase in the same program as we progressed through the objectives.

<br><br>
### Question:
Develop a Chat Box Server which allows multiple group chats. Each user will have its own unique user id and group id and can join any group chat. Multiple users having same group id will be placed in the same group. User can choose to disconnect and then join in any other group.


<br><br>
### Objective 1.
Develop a echo server-client program. A client sends a message to the server and the message is echoed back to the same client. The message is displayed in the client terminal. (same functionality as ‘echo’ command in Linux). Write only server program. No need to write client program. Use ‘telnet’ command to simulate the client.

 <br>
I developed the server program in Python 3 as I had experience working in socket programming. I had already developed a single group chat box as my side project. Experience from this project helped me a lot to ace the test. I used threading concept to accept connection requests and handle message relaying. One thread is used to accept random connection requests from clients. Other was to start a new thread for each client.


<br><br>
### Objective 2.
Develop a server program for multiple groups consisting of multiple clients. Each client will be asked the group id and accordingly will be placed in that group. If group does not exist, then create a new group with that id. Any message sent by a client will be relayed to other clients in that group.

<br><br>
### Objective 3:
Keep track of the chats. If any new client joins a group, then this client should receive all the previous chat messages in that group.

<br><br>
### Bonus Questions:
Store the messages in a persistent storage. If in case server is shut down and restarted, server should come back to its previous state.
Always store messages for not greater than 15 minutes. New client should receive chats happened in last 15 minutes only.


We were being evaluated by the Directi people during the test based on our approach and implementation. They also asked questions on how to scale this chat box to take it to production level such as database usage, persistent storage use for backup, etc.

I was able to solve all the three objectives and partially solved the bonus question. However, students who solved two questions were also shortlisted for further rounds. 7 students were selected for interview round. Link for server – client programs that I wrote as part of my project: [Project Link](https://bit.ly/2MFXBdz)


<br><br>
### F2F interview:
It was a technical interview and lasted for around 45 minutes. This was my first interview and so I was really nervous. It started with the all-time favorite question : ‘Tell me about yourself’. Then asked about project experience based on my resume. Then moved on to Networks and OS. I have experience working with startups and this proved quite helpful to explain them about my interests.



<br><br>

### Amongst the other questions asked to me, a few that I remember are as follows:
<br>
1. How is your experience in working with Linux systems?
2. What happens when you type ‘google.com’ in a web browser. Had to explain DNS look up, IP routing, NAT table.
3. Explain whole DNS message exchange process to convert URL to IP address.
4. What is subnetting? What is Network Id? Why do we use classless addressing?
5. Why do we use the concept of Private IPs and Public IPs?
6. Explain TCP and UDP and differentiate between the two. Why is UDP unreliable and TCP reliable and where can we use UDP?
7. What is system call?
8. What happens when a process encounters a function in its text?
9. Explain the 4 components of a process. (Stack, Heap, text, data)
10. Explain Loading and Linking

<br>
After the 1st round, I was told that I was selected for the 2nd round. They told me to prepare well as this is going to be a nightmare for me. But surprisingly, the 2nd round was not conducted for me (unlike my other peers who also had to go through a 2nd technical round). Also, there was no HR round.
<br>
The whole process went very smoothly and the Directi people were really helpful and encouraging.

Finally 3 students were offered the job.

I was one of them! 🙂
