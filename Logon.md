# Web Exploitation — picoCTF: Logon

## Introduction
The **Logon** challenge illustrates insecure session management vulnerabilities, demonstrating why client-side cookies should never be trusted for authorization and access control.

---

## Step 1: Analyzing the Login Portal
Open the challenge URL in your browser, which presents a basic authentication form requiring a username and password. 

1. Enter arbitrary or placeholder credentials (e.g., username: `joe`, password: `password`) into the login fields and submit the form.
2. Notice that the application logs you in successfully, but does not display the flag, indicating that authorization checks are handled separately from basic form completion.

---

## Step 2: Inspecting Cookies and Session Handling
Open your browser **Developer Tools**, navigate to the **Application** (or Storage) tab, and expand the **Cookies** section for the site.

* Upon logging in, the server issues specific session cookies: `username`, `password`, and `admin`.
* By default, the `admin` cookie is set to a boolean string value of `false`.

<img width="909" height="617" alt="image" src="https://github.com/user-attachments/assets/feb6b485-8c54-4d54-84d5-55bf4772ae8d" />

---

## Step 3: Modifying Session State
Because the application relies solely on client-side cookies to determine user privileges rather than performing robust server-side session validation:

1. Double-click the value of the `admin` cookie (currently set to `false`).
2. Change the value from `false` to `true`.

---

## Step 4: Refreshing and Capturing the Flag
With the `admin` cookie modified to `true`, refresh the page or navigate back to the dashboard endpoint. The application reads the updated cookie value, grants administrative access, and reveals the flag.
