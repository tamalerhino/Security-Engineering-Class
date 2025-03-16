# Month 1: Foundations in Web Security and Encryption
## Week 1: Introduction to Web Security Basics
**Topics:** HTTP, cookies, secure web browsing.

**Resources:**
- [Follow the Cookie Trail](https://www.youtube.com/watch?v=LHSSY8QNvew)  
- [Extra Follow the Cookie](https://www.youtube.com/watch?v=_d0G6FZ_kR4)  
- [Secure Web Browsing](https://www.youtube.com/watch?v=E_wX40fQwEA)  
- [Anatomy of a Web Request](https://www.realisable.co.uk/support/documentation/iman-user-guide/DataConcepts/WebRequestAnatomy.htm)  
- [MDN HTTP Overview (reference only, do not learn)](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)  
- [MDN HTTP Messages](https://developer.mozilla.org/en-US/docs/Web/HTTP/Messages)

**Lab:**
- Go through the TryHackMe labs, if you don't have an account sign up for one its free: 
   - [DNS in Detail](https://tryhackme.com/r/room/dnsindetail)  
   - [HTTP in Detail](https://tryhackme.com/r/room/httpindetail)  
   - [How Websites Work](https://tryhackme.com/r/room/howwebsiteswork)  
   - [Putting-It-All-Together](https://tryhackme.com/r/room/puttingitalltogether) 
- Go through the exercises from the video: [CURL API Testing Tutorial](https://www.youtube.com/watch?v=fVmHqtjFzbA) (Use [jsonplaceholder.typicode.com](https://jsonplaceholder.typicode.com/) for practice)
- Do additional exercises to further understand working with APIs: [APIs with Pokemon](Supporting%20Documents/APIs%20with%20Pokemon.md)


## Week 2: Encryption Basics
**Topics:** Encryption fundamentals, SP networks, Feistel Cipher, Magic numbers.

**Resources:**
- [Magic Numbers](https://www.youtube.com/watch?v=oJWwaQm-Exs&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=6)  
- [Superfish](https://www.youtube.com/watch?v=-enHfpHMBo4)  
- [SP Network](https://www.youtube.com/watch?v=DLjzI5dX8jc)  
- [One Encryption to Rule Them All](https://www.youtube.com/watch?v=VYech-c5Dic)  
- [Feistel Cipher](https://www.youtube.com/watch?v=FGhj3CGxl8I)  
- [Modes of Operation](https://www.youtube.com/watch?v=Rk0NIQfEXBA)

**Lab:** 
Follow this tutorial on practical basic encryption (no sign-up required):  
[Encryption](https://levelbuilder-studio.code.org/s/hoc-encryption/lessons/1/levels/1)

## Week 3: Symmetric Encryption
**Topics:** AES and AES GCM.

**Resources:**
- [AES](https://www.youtube.com/watch?v=O4xNJsjtN6E)  
- [AES GCM](https://www.youtube.com/watch?v=-fpVv_T4xwA&t=85s)  
- [AES Stick Guide (Just for fun)](https://www.moserware.com/2009/09/stick-figure-guide-to-advanced.html)

**Lab:** Go through the following exercise: [Practical AES Exercise](Supporting%20Documents/practical_aes_exercise.md)


## Week 4: Introduction to PKI & Digital Signatures
**Topics:** Public Key Infrastructure, digital signatures.

**Resources:**
- [PKI](https://www.youtube.com/watch?v=GSIDS_lvRv4)  
- [What Are Digital Signatures?](https://www.youtube.com/watch?v=s22eJ1eVLTU)
**Lab:** Go through the following exercise: Digital Signature Exercise with OpenSSL



# Month 2: Advanced Encryption Techniques & Secure Communications
## Week 1: TLS and Secure Protocols
**Topics:** TLS, SSL, Handshake, Diffie-Hellman.

**Resources:**
- [TLS](https://www.youtube.com/watch?v=0TLDTodL7Lc)  
- [TLS Handshake](https://www.youtube.com/watch?v=86cQJ0MMses)  
- [Another Explanation of TLS](https://www.youtube.com/watch?v=j9QmMEWmcfo)  
- [Diffie-Hellman](https://www.youtube.com/watch?v=NmM9HA2MQGI&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=1)  
- [Diffie-Hellman Math](https://www.youtube.com/watch?v=Yjrfm_oRO0w&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=2)  
- [Key Exchange Problems](https://www.youtube.com/watch?v=vsXMMT2CqqE&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=3)  
- [Elliptical Curves](https://www.youtube.com/watch?v=NF1pwjL9-DE&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=4)  
- [Elliptical Curve Backdoor](https://www.youtube.com/watch?v=nybVFJVXbww&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=5)

**Lab:** Go through the following exercise: TLS Exercise with OpenSSL


## Week 2: Cryptographic Hashing and HMAC
**Topics:** Hash functions (SHA), HMAC.

**Resources:**
- [Hashing Intro](https://www.youtube.com/watch?v=b4b8ktEV4Bg)  
- [Salting and Peppers](https://www.youtube.com/watch?v=--tnZMuoK3E)  
- [SHA Basics](https://www.youtube.com/watch?v=DMtFhACPnTY&list=PLvHL6JNW0PtM51fylnlpcuC9YeKSIyLiM&index=7)  
- [Hashing and Digital Signatures (HMAC)](https://www.youtube.com/watch?v=ODeivrc8Z_g&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=11)  
- [Additional HMAC Overview](https://www.youtube.com/watch?v=NytTScP4k7g&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=13)

**Lab:** Go through the following exercise: Hashing Exercise: Exploring Hash Functions with SHA-256


## Week 3: Introduction to HSMs
**Topics:** Hardware Security Modules (HSM).

**Resources:**
- [HSM Overview](https://www.youtube.com/watch?v=szagwwSLbXo)

**Lab:** No Lab - This would be similar to the AES and TLS exercise the only difference being it will be a hardware module vs a software module.


## Week 4: Practical PKI and Certificate Management
**Topics:** Deep dive into PKI, certificate chain of trust.

**Resources:**
- [PKI Series Part 1](https://www.youtube.com/watch?v=q9vu6_2r0o4&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=1)  
- [PKI Series Part 2](https://www.youtube.com/watch?v=5OqgYSXWYQM&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=2)  
- [PKI Series Part 3](https://www.youtube.com/watch?v=L1GkEnftoRQ&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=3)  
- [PKI Series Part 4](https://www.youtube.com/watch?v=lLw0dICMA_Y&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=4)  
- [PKI Series Part 5](https://www.youtube.com/watch?v=48TJ5fqnd3s&list=PLDp2gaPHHZK-mnKi3Zy_-hRjqLHh5PaAv&index=5)

**Lab:** Go through the TryHackMe lab, if you don't have an account sign up for one its free: 
- [Crypto Intro TryHackMe Lab](https://tryhackme.com/r/room/cryptographyintro)



# Month 3: Application(API) Security
## Week 1: API and AuthN/Z
**Topics:** What is an API? Basic understanding of Authentication and Authorization.

**Resources:**
- [API's Explained](https://www.youtube.com/watch?v=bxuYDT-BWaI)  
- [Authentication VS Authorization](https://www.youtube.com/watch?v=7ijBiXddB7w)  
- [Basic Authentication](https://www.youtube.com/watch?v=rhi1eIjSbvk)  
- [JWT Token](https://www.youtube.com/watch?v=7Q17ubqLfaM)  
- [Bearer Token](https://apidog.com/articles/what-is-bearer-token/#:~:text=third%2Dparty%20applications.-,What%20is%20a%20Bearer%20Token%3F)  
- [Factors of Authentication](https://www.youtube.com/watch?v=LB_lBMWH4-s)  
- [OAuth 2.0 Overview](https://www.youtube.com/watch?v=996OiexHze0)

**Lab:** Go through the following exercise: Authenticating to API's Using Github


## Week 2: SQL Injection
**Topics:** SQL Injection vulnerabilities.

**Resources:**
- [SQL Injection Explained](https://www.youtube.com/watch?v=_jKylhJtPmI)  
- [SQL Injection Examples](https://www.youtube.com/watch?v=ciNHn38EyRc)

**Lab:** 
- Go through the TryHackMe lab, if you don't have an account sign up for one its free: [SQL Injection Lab - TryHackMe](https://tryhackme.com/room/sqlilab)
- Additionally there are the Portswigger Labs go through the two first "Apprentice Labs" but feel free to keep going if you want more practice/scenarios: [PortSwigger SQL Labs](https://portswigger.net/web-security/all-labs#sql-injection)


## Week 3: XSS and CSRF Attacks
**Topics:** Cross-Site Scripting (XSS), Cross-Site Request Forgery (CSRF).

**Resources:**
- [XSS Basics](https://www.youtube.com/watch?v=L5l9lSnNMxg)  
- [Advanced XSS](https://www.youtube.com/watch?v=EoaDgUgS6QA)  
- [CSRF Overview](https://www.youtube.com/watch?v=vRBihr41JTo)  
- [CSRF in Practice](https://www.youtube.com/watch?v=eWEgUcHPle0)  
- Basic Security Headers
   - [Strict Transport Security](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Strict-Transport-Security)  
   - [Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP)  
   - [X-Content-Type-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Content-Type-Options)  
   - [X-Frame-Options](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-Frame-Options)  
   - [Referrer-Policy](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Referrer-Policy)  
   - [X-XSS-Protection](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/X-XSS-Protection)

**Lab:** Go through the following TryHackMe labs, if you don't have an account sign up for one its free:
- [XSS LAB (TryHackMe)](https://tryhackme.com/r/room/axss)  
- [Web App Basics (TryHackMe)](https://tryhackme.com/r/room/webapplicationbasics)  
- [Web App Security (TryHackMe)](https://tryhackme.com/r/room/introwebapplicationsecurity)  
- First 3 "Apprentice" labs on [PortSwigger XSS Labs](https://portswigger.net/web-security/all-labs#cross-site-scripting)


## Week 4: Break
Use this time to review or catch up on lessons.



# Month 4: Linux Fundamentals with Basic Networking and Firewalling
## Week 1: Introduction to Linux and the Command Line
**Topics:**
- Linux directory structure and essential commands (`ls`, `cd`, `mkdir`, `rm`, etc.)  
- Basic file manipulation and directory navigation.

**Resources:**
[50 most popular Linux commands](https://www.youtube.com/watch?v=ZtqBQ68cfJc) - Additional resource- very in depth and should only be used as reference - For now go through the lab section.

**Lab:**
- [Linux-Fundamentals-1 (TryHackMe)](https://tryhackme.com/r/room/linuxfundamentalspart1) (Part 2 or 3 are paid)  
- Follow these videos in a VM on devcloud or WSL:
    - [Linux For Hackers EP1](https://youtu.be/VbEx7B_PTOE?si=FcAp8dVpCcJvRJhZ&t=160)
    - [Linux For Hackers EP2](https://www.youtube.com/watch?v=A3G-3hp88mo)
    - [Linux For Hackers EP3](https://www.youtube.com/watch?v=Y17KTiJLcyQ&list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&index=3)


## Week 2: File and Directory Permissions
**Topics:**
- Linux file permissions and how to modify them (`chmod`, `chown`) 
- User and group management, understanding roles and permissions.
- Learn VIM!!!!!!!!!!

**Resources:**
- [Linux Users and Groups](https://www.youtube.com/watch?v=jwnvKOjmtEA&list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&index=4)  
- [Linux File Permissions](https://www.youtube.com/watch?v=LnKoncbQBsM)  
- [Learn VIM!!](https://www.youtube.com/watch?v=ggSyF1SVFr4)

**Lab:** Go through the following exercise: Linux User and Group Management Lab


## Week 3: Managing Services, Processes, and Basic Networking
**Topics:**
- Managing services using Systemd (start, stop, status)  
- Basic networking commands (`ifconfig`, `ping`, `netstat`, `ss`)  
- Introduction to firewalls (basic firewall rules)

**Resources:**
- [Installing packages](https://www.youtube.com/watch?v=vX3krP6JmOY&list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&index=5)  
- [Working with services](https://www.youtube.com/watch?v=wOWhfNB_r-0&list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&index=6)  
- [Killing services](https://www.youtube.com/watch?v=LfC6pv8VISk&list=PLIhvC56v63IJIujb5cyE13oLuyORZpdkL&index=7)  
- [Basic Linux Networking Commands](https://www.youtube.com/watch?v=MT85eMsMN6o)  
- [Introduction to Firewalls in Linux](https://www.youtube.com/watch?v=rL4-vbsN35w)( this could be alot of info, just take the basic concept of when a request comes in and gets accepted or blocked)
- [SELinux Explained](https://www.youtube.com/watch?v=gma-IRr5mnk&t) ( this is just scratching the surface there could be an entire course just on this topic, just get the basic concept of extra permissions on directories and services)

**Lab:** Go through the following TryHackMe labs, if you don't have an account sign up for one its free:
- [Linux File Analysis (TryHackMe)](https://tryhackme.com/r/room/linuxfilesystemanalysis)  
- [Linux Process Analysis (TryHackMe)](https://tryhackme.com/r/room/linuxprocessanalysis)  
- [Intro To Networking (TryHackMe)](https://tryhackme.com/r/room/introtonetworking)

## Week 4: Scripting Basics for Automation and Advanced Networking
**Topics:**
- Introduction to shell scripting for automating tasks.
- Automating network configurations and monitoring.
- Scheduling automated tasks with cron jobs.

**Resources:**
- [Linux Shell Scripting Tutorial Part 1](https://www.youtube.com/watch?v=SPwyp2NG-bE&list=PLIhvC56v63IKioClkSNDjW7iz-6TFvLwS&index=1)  
- [Linux Shell Scripting Tutorial Part 2](https://www.youtube.com/watch?v=7qd5sqazD7k&list=PLIhvC56v63IKioClkSNDjW7iz-6TFvLwS&index=2)  
- [Introduction to Cron Jobs](https://www.youtube.com/watch?v=7cbP7fzn0D8) (Follow along)
- [WAF Overview](https://www.cloudflare.com/learning/ddos/glossary/web-application-firewall-waf/)

**Lab:** Go through the following exercises:
- [Basic Bash Scripting (TryHackMe)](https://tryhackme.com/r/room/bashscripting)  
- [NMAP (TryHackMe)](https://tryhackme.com/r/room/nmap01)  
- WAF Exercise: Configuring and Testing a Basic WAF with ModSecurity


# Month 5: Understanding Programming, Version Control Basics, and Web Development Roles
## Week 1: Computer Architecture and Machine Code
**Topics:**
- Introduction to how computers process instructions at a low level.
- Concepts of CPU pipelines, binary logic, XOR, and simple logic gates.

**Resources:**
- [Machine Code Explained](https://www.youtube.com/watch?v=8VsiYWW9r48)  
- [CPU Pipeline](https://www.youtube.com/watch?v=BVNx3wtJ9vs&t=11s)  
- [Why Use Binary](https://www.youtube.com/watch?v=thrx3SBEpL8)

**Lab:** No lab


## Week 2: Secure Coding Practices
**Topics:**
- Introduction to secure coding principles, avoiding common vulnerabilities, and managing memory safely.
- Understanding garbage collection and why secure memory management matters.

**Resources:**
- [Garbage Collection Overview](https://www.youtube.com/watch?v=c32zXYAK7CI)

**Lab:**
No lab


## Week 3: Introduction to Front-End and Back-End Development
**Topics:**  
- Differences between Front-end and Back-end development  
- Common application architectures  
- **Front-end**: HTML, CSS, JavaScript, frameworks like React  
- **Back-end**: Server-side logic, databases, APIs, languages (Python, Java)

**Resources:**
- [Front End Development](https://www.youtube.com/watch?v=WG5ikvJ2TKA)  
- [Back End Development](https://www.youtube.com/watch?v=XBu54nfzxAQ)  
- [3-Tier Application Architecture](https://www.youtube.com/watch?v=r8JuAz9_V18)

**Lab:**
No lab


## Week 4: Git Version Control and Collaborative Development
**Topics:**
- Basics of Git, version control, and tracking changes in projects.
- Branching, merging, and collaborative workflows in Git.
- Managing secure code bases with Git.

**Resources:**
- [Git Overview](https://www.youtube.com/watch?v=92sycL8ij-U)  
- [How Git Works Internally](https://www.youtube.com/watch?v=bSA91XTzeuA)  
- [Git and Teams Using Git](https://www.youtube.com/watch?v=RzYJvSnzlMk)

**Lab:**
- [Learn Git Branching](https://learngitbranching.js.org/?locale=en_US)  
  (Do the first 4 levels of "Main" and first 8 levels of "Remote")


# Month 6: Python Programming Fundamentals
## Week 1 & 2 : Introduction to Python Basics
**Topics:**  
- Basic syntax  
- Variables  
- Data types  
- Conditional Statements

**Resources:**
- [Python Programming 2024 Course](https://programming-24.mooc.fi/part-1)

**Lab:** Get through the first 7 parts of Introduction to Programming


## Week 3: Continued Introduction to Python Basics
**Topics:**  
- Objects, Methods, and Classes  

**Resources:**
- [Python Programming 2024 Course](https://programming-24.mooc.fi/part-1)

**Lab:** Go through parts 8-14 


## Week 4: Project: Password Strength Checker
**Project Goals:**  Develop a Python script that evaluates the strength of a password based on length, character variety, and uniqueness.

** Features to Implement:** 
- Accept user input for a password.
- Provide feedback on password strength (e.g., weak, moderate, strong) based on specific criteria.
- Suggest improvements for weak passwords, such as adding special characters, increasing length, or mixing character cases.

**Extension Ideas:** Incorporate a list of common weak passwords to warn users if they’re using one of them.



# Month 7: Advance Python Programming and Databases 
## Week 1: Introduction to Databases and SQL Basics
**Topics:**
- Understanding databases and SQL.
- Basics of SQL: creating tables, inserting data, and retrieving data.

**Resources:**
- [What is a database?](https://www.youtube.com/watch?v=Tk1t3WKK-ZY)  
- [SQL Basics Video](https://www.youtube.com/watch?v=xiUTqnI6xk8)  
- [SQL cheat sheet](https://images.datacamp.com/image/upload/v1714149594/Marketing/Blog/SQL_for_Data_Science.pdf)

**Lab:**
- Go through the first 4 lessons (or more) on [SQLBolt](https://sqlbolt.com/)


## Week 2: Setting Up SQLite with Python
**Topics:**
- Introduction to SQLite (lightweight database in Python)  
- Using the `sqlite3` library  

**Resources:**
- [Python and SQLite Database Tutorial](https://www.youtube.com/watch?v=byHcYRpMgI4) (watch until "Insert Many Records Into Table")

**Lab:**
- Create your own database
- Set up a simple SQLite database in Python, create a table, and add data to it.
- Write Python scripts to insert, and delete data within the SQLite database.


## Week 3: Querying and Retrieving Data in Python
**Topics:**  
- Using `SELECT` statements in SQL  
- Filtering/sorting with `WHERE` and `ORDER BY`  
- Reading/processing results in Python  

**Resources:**
- [SQL Queries reference](https://www.youtube.com/watch?v=byHcYRpMgI4&t=2081s)(same link as above but will put you directly on how to select data)

**Lab:**
- From your own database you created in the previous lab.
- Use Python to query the database and filter results based on conditions.
- Implement simple data processing (e.g., sum, average) on retrieved data.


## Week 4: Building a Simple Python Application with Database Project
Putting it all together by creating a Python application that interacts with a database.

**Project Details:**  Personal Task Manager
Create a basic Python application - Personal Task Manager that allows:
- Adding new records.
- Viewing all records.
- Updating or deleting records.

**Tasks:**
- Add, update, delete, and mark tasks as complete.
- Store tasks in a SQLite database, with fields like id, task_name, due_date, and status.
- Retrieve and display upcoming tasks, sorted by due date.
- Write SQL queries to handle each function within the application.

**Learning Outcomes:** 
- Integrating Python and SQL commands effectively.
- Building CRUD (Create, Read, Update, Delete) functionality in a real application.



## Month 8: Threat Modeling
# Week 1: Introduction to Threat Modeling Fundamentals
**Topics:**  
- Understanding threat modeling, purpose, key concepts (assets, threats, vulnerabilities, controls)  
- Identifying potential attack surfaces

**Resources:**
- [Threat Modeling Manifesto](https://www.threatmodelingmanifesto.org/)  
- [Threat modeling intro](https://www.youtube.com/watch?v=h_BC6QMWDbA)  
- [Cybersecurity Architecture](https://www.youtube.com/watch?v=jq_LZ1RFPfU)  
- [Security Controls](https://www.youtube.com/watch?v=4i0QTTJbVGU)

**Lab:**
- [Security Principles (TryHackMe)](https://tryhackme.com/r/room/securityprinciples)  
- [Secure Network Architecture (TryHackMe)](https://tryhackme.com/r/room/introtosecurityarchitecture)  
- [OWASP Top 10 (TryHackMe)](https://tryhackme.com/r/room/owasptop102021)

## Week 2 & 3: Common Threat Modeling Methodologies
**Topics:** STRIDE, DREAD, PASTA, and LINDDUN methodologies.

**Resources:**
- [STRIDE](https://www.youtube.com/watch?v=rEnJYNkUde0)  
- [DREAD](https://www.youtube.com/watch?v=4acynfRM6ws)  
- [PASTA (reference)](https://threat-modeling.com/pasta-threat-modeling/) (Not a video, any video i found for PASTA was over an hour long..)
- [LINDDUN](https://www.youtube.com/watch?v=zq-L86Xhi_Y)  
- [MITRE ATT&CK](https://www.youtube.com/watch?v=Yxv1suJYMI8)  
- [Lockheed Martin Kill Chain](https://www.youtube.com/watch?v=II91fiUax2g) (Not threat modeling but its what we use after we find out there has been a breach)
- [OWASP Threat Modeling Cheat Sheet (reference)](https://cheatsheetseries.owasp.org/cheatsheets/Threat_Modeling_Cheat_Sheet.html) (For reference only!)

**Lab:**
- [Intro to Detection Engineering (TryHackMe)](https://tryhackme.com/r/room/introtodetectionengineering)  
- [STRIDE Threat modeling (video)](https://www.youtube.com/watch?v=Wry2get_RRc) (follow along!)

## Week 4: Break
Break



# Month 9: CI/CD Fundamentals, S-SDLC and Basic Pipelines with Jenkins
## Week 1: Introduction to CI/CD Concepts and Pipeline Basics
**Topics:**
- Overview of Continuous Integration and Continuous Deployment.
- Key CI/CD concepts: automated builds, testing, deployment, and rollback.
- Benefits of CI/CD for software development and DevOps.

**Resources:**
Go through the labs

**Lab:**
- [Intro to DevSecOps (TryHackMe)](https://tryhackme.com/r/room/introductiontodevsecops)  
- [Intro to SDLC (TryHackMe)](https://tryhackme.com/r/room/sdlc)  
- [Intro to S-SDLC (TryHackMe)](https://tryhackme.com/r/room/securesdlc)  
- [Intro to Pipeline Automation (TryHackMe)](https://tryhackme.com/r/room/introtopipelineautomation)  
- [Intro to IaC (TryHackMe)](https://tryhackme.com/r/room/introtoiac)


## Week 2: Setting Up Jenkins and Creating Your First Pipeline
**Topics:**
- Introduction to Jenkins: installation, interface overview, and key features.
- Setting up a simple Jenkins project and pipeline.

**Resources:**
- [Getting Started with Jenkins](https://www.youtube.com/watch?v=6YZvp2GwT0A)

**Lab:**
- [Build a Python App with Jenkins](https://www.jenkins.io/doc/tutorials/build-a-python-app-with-pyinstaller/)

## Week 3 &4: Project: Create a Full CI/CD Pipeline in Jenkins
**Project Overview:**
Build a full CI/CD pipeline using Jenkins to automate the workflow for a simple application.
**Features to Implement:**
- **Source Control Integration:** Automatically trigger the pipeline when code is committed to the repository.
- **Build and Test Automation:** Automate the building and testing of the application, with test results published in Jenkins.
- **Deployment Automation:** Deploy the application to a staging environment.
- **Notifications:** Configure notifications for pipeline status updates.
**Extension Ideas:**
Set up pipeline triggers based on different branches (e.g., separate staging and production).

# Month 10: Basics of Containerization with Docker
## Week 1: Introduction to Containerization
**Topics:**
- What are containers  
- Benefits of containerization  
- Containers vs Virtual Machines

**Resources:**
- Ulises Containerization Class (Recording coming soon)
- [Containerization Basics](https://www.youtube.com/watch?v=0qotVMX-J5s)

**Lab:**
- [Intro to Containerization (TryHackMe)](https://tryhackme.com/r/room/introtocontainerisation)

## Week 2: Understanding Docker and Dockerfiles
- Docker basics  
- Creating Dockerfiles  
- Commands: `docker build`, `docker run`, `docker images`, `docker ps`

**Resources:**  
- [Docker 101: Dockerfile Basics](https://www.youtube.com/watch?v=eGz9DS-aIeY&list=PLIhvC56v63IL2OjFvv_PI0B2yAXGfJLMI&index=9)  
- [Dockerfile Reference Documentation](https://docs.docker.com/reference/dockerfile/)

**Lab:**  
- [Intro to Docker (TryHackMe)](https://tryhackme.com/r/room/introtodockerk8pdqk)

## Week 3: Building and Managing Containers
**Topics:**  
- Building images  
- Running/managing containers  
- Container lifecycle  
- Tagging and pushing images

**Resources:**  
- [Building a Custom Docker Image](https://www.youtube.com/watch?v=ZGw-Jr1lHYA)  
- [Container Management](https://www.youtube.com/watch?v=nFeJum_UuMg)  
- [Dockerhub 101](https://www.youtube.com/watch?v=mAzHELZWE-Y)

**Lab:** Build, tag, and push a Docker image to Docker Hub (or a private registry if available).

## Week 4: Networking and Managing Persistent Data in Containers
**Topics:**  
- Docker networking basics  
- Exposing ports  
- Using volumes for data persistence

**Resources:**
- [Docker Networking Basics](https://www.youtube.com/watch?v=bKFMS5C4CG0&list=PLIhvC56v63IJlnU4k60d0oFIrsbXEivQo&index=4)  
- [Volumes in Docker](https://www.youtube.com/watch?v=p2PH_YPCsis)

**Lab:**  
- Create a container (e.g., Nginx or simple web server) with exposed port and persistent volume


# Month 11: Secure coding and intro to Supply Chain Security
## Week 1: Introduction to Secure Coding in Python
**Topics:**
- Overview of secure coding practices in Python.
- Common security pitfalls: insecure data handling, input validation, and logging.

**Resources:**  
- [Code Formatting with Black](https://www.youtube.com/watch?v=A6S2nZAXgT8)  
- [Code Securely with Bandit](https://www.youtube.com/watch?v=YZOKnvisJpw)  
- [Static type checking with Mypy](https://www.youtube.com/watch?v=9gNnhNxra3E)

**Lab:**
Follow along with the videos

## Week 2: Software Supply Chain Security and Dependency Management
**Topics:**
- Introduction to software supply chain security and dependency management.
- Risks of open-source libraries, dependency confusion, and supply chain threats.

**Resources:**
**Resources:**  
- [Introduction to Software Supply Chain Security](https://www.youtube.com/watch?v=F2FfaSX_55A)  
- [SBOMs](https://www.youtube.com/watch?v=H3UqVumgUFQ)

**Lab:**  
- [SCA with Snyk (TryHackMe)](https://tryhackme.com/r/room/snykcode)


## Week 3: Software Supply Chain Security Tools
**Topics:**
Tools for software supply chain security 

**Resources:**
- [Trivy (SCA)](https://www.youtube.com/watch?v=BtICIgcnaF0)  
- [CodeQL (SAST)](https://www.youtube.com/watch?v=8XSf6XfYl64&list=PLX8G9idOAfzg3uTfdAgDkybK9CG71vsaq&index=4)  
- [Checkmarx (SAST)](https://www.youtube.com/watch?v=FV9bdKt0dSA)  
- [SonarQube (SAST & SCA)](https://www.youtube.com/watch?v=xeTwG9XFFTE) (Although its used more for Code Smells and Best Practices)
- [Open Policy Agent (OPA)](https://github.com/tamalerhino/opa)  
- [Gatekeeper (Kubernetes + OPA)](https://github.com/tamalerhino/gatekeeper)(like OPA but for Kubernetes)

**Lab:** Using Trivy for SCA on a Basic Web Application

## Week 4: Final Project - Build a Secure CI/CD Pipeline with Supply Chain and Code Scanning
**Project Goals:** Develop a secure CI/CD pipeline to automate secure coding and dependency management checks.
**Features to Implement:** (TBD on where to implement this - the previous week teaches you how to stand a jenkins on your VM)
- **CI/CD Pipeline Setup:** Set up a basic CI/CD pipeline using GitHub Actions or a similar tool.
- **SCA with Trivy:** Integrate Trivy for Software Composition Analysis (SCA) to scan for known vulnerabilities in dependencies.
  - **Command:** `trivy fs .` (for local file scanning)
- **SAST with CodeQL:** Add CodeQL for Static Application Security Testing (SAST) to analyze code for security weaknesses.
    - **Command:** Use CodeQL workflows in GitHub Actions for automated scans.
- **Automated Dependency Checking:** Configure OWASP Dependency-Check to run with every build to flag insecure packages automatically.
**Documentation Tasks:** 
- Document supply chain risks and describe mitigation strategies.
- Create a threat model, identifying dependencies and potential risks in the supply chain.
- List steps for ongoing security maintenance, such as regular updates and re-scanning dependencies.
**Extension Ideas:** 
Set up automated notifications for outdated packages, and periodically check for newer secure library versions.
Experiment with additional tools like Bandit for Python-specific security scanning and Docker Bench if containerized applications are in use.



# Month 12: Cloud Security Fundamentals
## Week 1: Introduction to Cloud Security and Cloud Service Models
**Topics:**
- Overview of cloud computing and its service models (IaaS, PaaS, SaaS).
- Shared Responsibility Model in cloud security.

**Resources:** All Resources are on Pluralsight through degreed Make sure you are logged into degreed first
- [What is Cloud Security?](https://www.youtube.com/watch?v=jI8IKpjiCSM)  
- AWS Cloud Terms
- [AWS Certified Developer - Associate (DVA-C02): Beginner's Guide to EC2](https://www.pluralsight.com/courses/aws-certified-developer-associate-dva-c02-beginners-guide-to-ec2)
- [AWS Shared Responsibility Model](https://aws.amazon.com/compliance/shared-responsibility-model/)

**Lab:**
Watch these videos and follow along on in our AWS Sandbox account - Ask Ulises how to login
- AWS Fundamental Services


## Week 2: Identity and Access Management (IAM)
**Topics:**
- Importance of Identity and Access Management in the cloud.
- Principles of least privilege, multi-factor authentication (MFA), and roles vs. users.

**Resources (via Pluralsight):**  
- [AWS Identity and Access Management Fundamentals](https://degreed.com/courses/aws-identity-and-access-management-fundamentals)

**Lab (via A Cloud Guru/Pluralsight):**  
- [Introduction to AWS IAM](https://app.pluralsight.com/hands-on/labs/4b620748-f44f-408a-a42b-f727a208e952)  
- [Understanding IAM and Basic Network Security in the Cloud](https://app.pluralsight.com/hands-on/labs/5c3fffce-2a89-414f-acab-1156a7175299)  
- [Create Users and Manage Permissions Using Groups and Policies in IAM](https://app.pluralsight.com/hands-on/labs/28b414c4-8407-476d-bdbf-9bfc0b395320)  
- [Managing AWS IAM User Permissions Using Groups and Policies](https://app.pluralsight.com/hands-on/labs/4b52d9c3-b09d-4dd5-8117-42c67bc26354)  
- [Creating an IAM Role and Configuring an EC2 Instance for AWS Systems Manager](https://app.pluralsight.com/hands-on/labs/41fa20fe-7199-4a0a-a02c-e86fb26613c8)  
- [Creating and Assuming an Administrator AWS IAM Role](https://app.pluralsight.com/hands-on/labs/e76243b6-7a8a-412c-b9c9-7ea2a4a78978)  
- [Monitoring, Auditing, and Logging in AWS IAM](https://app.pluralsight.com/hands-on/labs/9c173560-f318-4a3a-97fa-341bdbdc76a3)


## Week 3: Network Security in the Cloud
**Topics:**
- Virtual Private Cloud (VPC), security groups, and firewall rules.
- Configuring secure network architectures and using private/public subnets.

**Resources (via Pluralsight):**  
- [AWS Networking Fundamentals](https://app.pluralsight.com/library/courses/aws-networking-fundamentals/table-of-contents)  
- [Implementing AWS Networking Security Groups](https://app.pluralsight.com/library/courses/implementing-aws-networking-security-groups/table-of-contents)  
- [AWS Networking Deep Dive: ELB](https://app.pluralsight.com/library/courses/aws-networking-deep-dive-elb/table-of-contents)  
- [AWS Networking Deep Dive: Route 53 DNS](https://app.pluralsight.com/library/courses/aws-networking-deep-dive-route-53-dns/table-of-contents)  
- [AWS Networking and the API Gateway](https://app.pluralsight.com/library/courses/aws-networking-api-gateway/table-of-contents)  
- [Delivering Content on AWS with Amazon CloudFront](https://app.pluralsight.com/library/courses/cloudfront-aws-delivering-content/table-of-contents)  
- [AWS Networking Deep Dive: VPC](https://app.pluralsight.com/library/courses/aws-networking-deep-dive-vpc/table-of-contents)

**Lab (A Cloud Guru/Pluralsight):**  
- [Create a VPC and Launch an EC2 Instance](https://app.pluralsight.com/hands-on/labs/39a6f5c7-7590-4bd5-beca-e3c310be919e)  
- [Creating a Basic VPC and Components in AWS](https://app.pluralsight.com/hands-on/labs/2cc3cf9e-61ce-475d-a00e-03306e9ba285)  
- [Launch an EC2 Instance in a VPC](https://app.pluralsight.com/hands-on/labs/5b14955f-1d70-4a0a-9a11-61858fb5e17c)  
- [Creating and Configuring a Network Load Balancer in AWS](https://app.pluralsight.com/hands-on/labs/a0c93cdb-127d-43e5-9026-aea0a8dc5c5d)  
- [Configuring Network Integration with Application Services](https://app.pluralsight.com/hands-on/labs/ffd8e120-bbb7-4cdc-99ae-6312b03eb85c)  
- [Configuring an AWS Network Firewall](https://app.pluralsight.com/hands-on/labs/06ea5cd8-8eb8-4e3a-a679-715f820ee637)  
- [Creating and Validating Connectivity for EC2 Instances in Public/Private Subnets](https://app.pluralsight.com/hands-on/labs/3e0d1d6a-f5c0-48ea-a09d-f3e9d222cf6f)  
- [Enable IPv6 on a VPC with a Private Subnet](https://app.pluralsight.com/hands-on/labs/4d0437f6-7288-4233-bba5-f7c1a0895a11)  
- [Building a Three-Tier Network VPC from Scratch in AWS](https://app.pluralsight.com/hands-on/labs/f2a24706-8b7b-4a21-9ad6-859bd5595215)  
- [Troubleshooting AWS Network Connectivity: Security Groups/NACLs](https://app.pluralsight.com/hands-on/labs/cffb7f13-1c46-45cb-886a-f0bb12ff038c)

## Week 4: Data Security and Compliance in the Cloud
**Topics:**
- Data encryption at rest and in transit.
- Key Management Services (KMS) and cloud provider encryption options.
- Introduction to compliance (GDPR, HIPAA) and logging/auditing.

**Resources (via Pluralsight):**  
- [AWS Networking Fundamentals](https://app.pluralsight.com/library/courses/aws-networking-fundamentals/table-of-contents)  
- [Storing Data on AWS](https://app.pluralsight.com/library/courses/storing-data-aws/table-of-contents)  
- [Implementing Amazon S3 Storage on AWS](https://app.pluralsight.com/library/courses/aws-s3-implementing/table-of-contents)  
- [AWS Certified Solutions Architect – Associate (SAA-C03): Databases and Machine Learning](https://app.pluralsight.com/ilx/aws-certified-solutions-architect-associate-(saa-c03)-databases-and-machine-learning/table-of-content)  
- [AWS Certified Security – Specialty (SCS-C02): Data Protection](https://app.pluralsight.com/ilx/aws-certified-security-specialty-(scs-c02)-data-protection/table-of-content)  
- [Monitoring AWS Cloud Security](https://app.pluralsight.com/library/courses/aws-cloud-security-monitoring/table-of-contents)  
- [Introduction to AWS CloudTrail](https://app.pluralsight.com/library/courses/introduction-aws-cloudtrail/table-of-contents)

**Lab (A Cloud Guru/Pluralsight):**  
- [Creating S3 Buckets with Versioning and Encryption](https://app.pluralsight.com/hands-on/labs/690ec911-7b3a-4dd3-88a3-1a6b5a82c44c)  
- [Creating and Securing Customer Managed Keys with AWS KMS](https://app.pluralsight.com/hands-on/labs/721b54b8-34b5-407b-9deb-c98681792ef8)  
- [Moving a MySQL Database to AWS](https://app.pluralsight.com/hands-on/labs/68b15e5a-6295-4e22-a1c6-fbe7aa23918f)  
- [Working with AWS VPC Flow Logs for Network Monitoring](https://app.pluralsight.com/hands-on/labs/b4c238b3-92e4-47d9-96b1-3ef744fa999e)  
- [Standing Up an Apache Web Server EC2 Instance and Sending Logs to Amazon CloudWatch](https://app.pluralsight.com/hands-on/labs/920e2b8e-5c4c-497d-9383-d7cc73ecb9ac)  
- [Configure an Alert Based on Logging Content](https://app.pluralsight.com/hands-on/labs/f669e144-3568-4a8a-ab6b-0dc19b295c27)  
- [Creating a CloudTrail Trail and EventBridge Alert for Console Sign-Ins](https://app.pluralsight.com/hands-on/labs/f3e23824-baf8-4937-aefd-9b50ac1ecce9)  
- [AWS Access Control Alerts with CloudWatch and CloudTrail](https://app.pluralsight.com/hands-on/labs/a3839dd5-7088-4941-9e7e-fd04f006ccd2)  
- [Identifying and Remediating Threats with AWS Security Hub](https://app.pluralsight.com/hands-on/labs/572af34e-00c4-45a4-9a68-4a2e8f0c79d6)

# Final Project: Deploy an app in the cloud
For a practical wrap-up project, deploy a small application that you have coded, and containerized on the cloud.

**Project Steps:**
- Set up a secure VPC with public and private subnets.
- Deploy a simple app (e.g., a web server) use RDS as your backend database.
- Apply IAM roles with least privilege.
- Configure security groups for specific access,
- Enable encryption for stored data on RDS and/or S3
- Set up logging, monitoring and alerting for your app using cloudwatch and cloudtrail
- **BONUS:** Use codeploy or a CI to deploy your entire application using a CI tool.
**Learning Outcomes:**
Put it all together to understand security configurations and apply them in a real-world scenario.
