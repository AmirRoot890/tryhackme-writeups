# TryHackMe – Offensive Security Intro

Room Link: https://tryhackme.com/room/offensivesecurityintro  
Level: Beginner  
Category: Offensive Security / Web  

---

## Overview
This room provides an introduction to Offensive Security and demonstrates how attackers identify and exploit vulnerabilities in web applications.
The lab focuses on directory enumeration and business logic flaws using a vulnerable banking website.

---

## Task 1 – What is Offensive Security?

### Objective
Understand the concept of Offensive Security and how attackers think.

### Summary
Offensive Security involves legally attacking systems to discover vulnerabilities before malicious actors do.
It is commonly used in penetration testing and red team operations.

The main goal is to think like an attacker and identify weaknesses such as:
- Hidden endpoints
- Broken access controls
- Business logic flaws

---

## Task 2 – Starting the Lab

### Objective
Deploy and prepare the lab environment.

### Actions Taken
- Started the target virtual machine
- Accessed the web application
- Verified the environment was ready for testing

---

## Task 3 – Your First Hack

### Objective
Enumerate hidden directories on the web server.

### Tool Used
dirb – a web directory brute-forcing tool.

### Command Used
dirb http://fakebank.thm

### Discovered Paths
- /bank-deposite
- /images

### Analysis
These directories were not visible on the main page.
The presence of sensitive functionality in hidden paths indicates poor access control and misconfiguration.

---

## Task 4 – Adding Funds to Your Account

### Objective
Exploit a business logic flaw to add funds to an account.

### Exploitation
- Accessed the /bank-deposite endpoint
- Added funds without authentication or authorization
- The application did not validate account ownership

### Result
BANK-HACKED

### Vulnerability Type
- Broken Access Control
- Business Logic Flaw

---

## Summary

Task 1: Learn Offensive Security – Completed  
Task 2: Start the lab – Completed  
Task 3: Directory enumeration – /bank-deposite, /images  
Task 4: Logic flaw exploitation – Flag captured  

---

## Key Takeaways
- Offensive Security requires attacker-style thinking
- dirb is essential for web reconnaissance
- Business logic flaws can be highly critical
- Hidden directories are common attack vectors
