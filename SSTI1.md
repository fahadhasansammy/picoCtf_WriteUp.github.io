# Web Exploitation — picoCTF 2025: SSTI1

## Introduction
The **SSTI1** challenge demonstrates Server-Side Template Injection (SSTI), a vulnerability that occurs when user-supplied input is unsafely concatenated or embedded directly into a web template engine, allowing code execution or evaluation on the server.

---

## Step 1: Exploring the Web Application
Open the challenge link provided in the platform description. You will see a web page allowing you to make announcements or input custom text strings.

<img width="1608" height="361" alt="image" src="https://github.com/user-attachments/assets/02684ac3-a4f5-4f61-903f-10a6684635c8" />

---

## Step 2: Testing for Template Injection
Because the description hints that "templating is a cool and modular way to build web apps," test the input field for template evaluation behaviors by submitting a standard mathematical expression wrapped in template syntax:

`{{7*7}}`

If the application is vulnerable to Server-Side Template Injection, it will evaluate the expression server-side instead of printing it literally.

<img width="559" height="225" alt="image" src="https://github.com/user-attachments/assets/9810243c-7200-4388-9743-a7be8ed536b2" />

---

## Step 3: Exploiting SSTI to Retrieve the Flag
Craft a template payload tailored to the underlying backend engine (such as Jinja2 for Python/Flask) to access configuration objects, environment variables, or execute commands that expose the target flag.

Submit the payload, observe the server's processed output, and capture the flag.

<img width="1888" height="506" alt="image" src="https://github.com/user-attachments/assets/4026feb7-ce63-4a9d-8c43-06a17889dd5b" />
