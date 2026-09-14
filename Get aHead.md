Web Exploitation PicoCTF:Get aHead
The CyLab Security Academy (picoCTF) is an excellent platform for practicing web exploitation with a wide variety of challenges. One beginner-friendly challenge is named Get aHEAD.

Step 1: Explore the Application
Open the challenge link to view the main page, which features two interactive buttons.
<img width="1100" height="522" alt="image" src="https://github.com/user-attachments/assets/c0c4ff79-0126-491f-bba5-a9d4e953947a" />


Step 2: Intercept the Traffic

Open Burp Suite and turn on intercept to capture the HTTP request generated when clicking either button. The proxy will show an incoming GET request.

<img width="720" height="583" alt="image" src="https://github.com/user-attachments/assets/4acfb70f-6de9-48fd-b2ed-c701a255d7de" />
<img width="720" height="583" alt="image" src="https://github.com/user-attachments/assets/b56f1784-57f7-4f0c-a25c-763eb48ecdc2" />

Step 3: Use the Repeater

Become a Medium member
Send the captured GET request to Burp Repeater. As hinted by the challenge name ("Get aHEAD"), the objective involves HTTP method manipulation.

<img width="720" height="233" alt="image" src="https://github.com/user-attachments/assets/56743518-7ded-4e3a-be26-c061f98a4396" />

Step 4: Modify the HTTP Method

Replace the GET method in the request line with HEAD.

<img width="738" height="238" alt="image" src="https://github.com/user-attachments/assets/7aab939d-15e7-4442-9bea-e10f6b1848cd" />

Step 5: Retrieve the Flag

Click Send in the Repeater. The server’s response header will contain the hidden flag.
