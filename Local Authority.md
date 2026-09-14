# Web Exploitation — picoCTF: Local Authority

## Introduction
The **Local Authority** challenge introduces common web reconnaissance techniques, demonstrating why relying on client-side authentication checks and hiding sensitive endpoints in frontend scripts is insecure.

---

## Step 1: Initial Reconnaissance & Inspecting the Page
Open the challenge URL provided in your browser. 

1. Right-click anywhere on the webpage and select **Inspect** (or press `Ctrl+Shift+I`) to open the browser Developer Tools.
2. Review the HTML structure and network traffic to understand how the application handles user input.

<img width="1914" height="143" alt="Challenge Main Page" src="https://github.com/user-attachments/assets/62788be3-db7f-488c-b066-a30a9844fad6" />

---

## Step 2: Discovering Hidden Endpoints
When standard directory navigation or application flow isn't immediately obvious, inspect form actions or check for common administrative and login pages (such as `/login.php`). Append `/login.php` to the base URL in your browser address bar:

`http://saturn.picoctf.net:63195/login.php`

---

## Step 3: Analyzing Application Files
Navigating to the login portal presents the authentication interface. 

<img width="719" height="303" alt="Login Portal Interface" src="https://github.com/user-attachments/assets/896e5124-8d64-4f7f-a207-5befb35ae45a" />

---

## Step 4: Investigating Source Code & Client-Side Scripts
In Developer Tools, navigate to the **Sources** or **Debugger** tab to review loaded JavaScript files. 

<img width="683" height="328" alt="Source Files Inspector" src="https://github.com/user-attachments/assets/4c48dcef-2da5-4e65-b3da-4aa73dbd81a8" />

---

## Step 5: Extracting Credentials & Capturing the Flag
Upon reviewing the client-side validation scripts linked in the source, you can locate the hardcoded username and password values used by the script to authenticate users insecurely on the frontend. Use these credentials to log in and retrieve the flag.
