# fahadhasansammy.github.io
Web Exploitation — picoCTF: Where are the robots?

Introduction:
This challenge introduces a common reconnaissance flaw involving the robots.txt file, which developers often mistakenly use to hide sensitive directories from public view.

Step 1: Inspecting the robots.txt File
Open the provided challenge link. To see what paths the website owner is attempting to hide, append /robots.txt directly to the end of the URL in your browser address bar and press Enter.
<img width="1913" height="332" alt="Screenshot 2026-09-13 143107" src="https://github.com/user-attachments/assets/02f82dc1-006e-4593-86b6-2236002e4ecc" />

Step 2: Locating the Disallowed Directory

Review the contents of the robots.txt file. You will see a line similar to:
Disallow: /cc6b1.html
<img width="975" height="150" alt="image" src="https://github.com/user-attachments/assets/0432f086-dcec-41e7-b7b0-4c68284a2779" />
This entry reveals a restricted path or hidden file that search engines (and ordinary users) are discouraged from visiting.

Step 3: Retrieving the Flag
Copy the disallowed path (/cc6b1.html) and append it to your base application URL in the browser address bar. Pressing Enter will take you directly to the hidden page, where the flag is displayed.
<img width="975" height="505" alt="image" src="https://github.com/user-attachments/assets/9a1f814a-9e4d-4224-b254-1dc076653278" />
