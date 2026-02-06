


## Introducing Today's Project!

In this project I built a CLI command told that identifes code  vulnerabilities to various attacks like hardcoded secrets, SQL injection, and weak crytography. I am interested in this because companies like Google amd Synk utilize AI to spot vulnerabilities in code early so they dont become a larger problem in production.

### Key tools and concepts

Tools I used were python, Gemini. Key concepts I learnt include environment variables, Gemini API and code security. I did this project because I wanted to learn how to make code less vulnerable using Gemini API. This project met my goals by improving my understanding around what vulnerable code looks like and how to avoid it getting into production. Next, I plan to implement multiple file scanning.

---

## Connecting to Gemini API

In this step, I'm setting up the Gemini API connection. This involves creating an .env filr and adding the Gemini API key to it. I need to do this so I can test and verify my connection to Gemini


![Image](http://learn.nextwork.org/triumphant_cyan_clever_dragonfly/uploads/ai-security-audit_sec2c3d4)

I verified the connection by running "python scanner.py". Gemini responded with "Hello, security scanner!" which confirmed that that API is connected to Google's services

![Image](http://learn.nextwork.org/triumphant_cyan_clever_dragonfly/uploads/ai-security-audit_sec4e5f6)

My scanner.py file works by sending a propmt to Gemini with the code. When I ran it, Gemini identified sereval issues(plain text password, no hashing and more) and ranked them by level of importance. This shows that the Gemini API can detect vulnerabilities.

---

## Building the Vulnerability Scanner

In this step, I'm building a vulnerability scanner that will detect SQL Injection, hardcoded secrets and weak passwords. This will allow me to write secure and deployable code 

![Image](http://learn.nextwork.org/triumphant_cyan_clever_dragonfly/uploads/ai-security-audit_sec7h8i9)

The vulnerabilities Gemini detected were SQL Injection, hardcoded secrets and a weak hashing algorithm. The security prompt I crafted asked for the vulnerability type, why, the impact and a remediation This structured output helps me identify the vulnerabilities abd resolve the issue.

---

## Adding Severity Ratings

In this step, I'm adding severity ratings which with color coded outputs (CRITICAL, HIGH, MEDIUM, LOW) . I'm also installing colorama for colored terminal output.

![Image](http://learn.nextwork.org/triumphant_cyan_clever_dragonfly/uploads/ai-security-audit_sec0k1l2)

I updated the security prompt to include a severity ratings. The add_colors_to_output function works by replacing existing text with colored text using colorama library. When I see CRITICAL in red, it tells me needs an immediate remediation.

---

## Scanning Real Python Files

I'm adding file reading capabilities to the scanner. This lets the scanner accepts command-line arguments for file paths. 

![Image](http://learn.nextwork.org/triumphant_cyan_clever_dragonfly/uploads/ai-security-audit_sec3n4o5)

---


---
