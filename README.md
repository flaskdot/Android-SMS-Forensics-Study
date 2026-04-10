# Android-SMS-Forensics-Study
"A research project to demonstrate the vulnerabilities of local SMS storage in Android and how to analyze message integrity for digital forensics."
# SMS Integrity & Forensics Study Tool

## 1. Project Overview
This project is a technical demonstration for a graduation thesis. It explores how the Android Operating System stores SMS messages and evaluates the security measures preventing unauthorized data manipulation.

## 2. Technical Scope
* **Data Store:** SQLite Database (`mmssms.db`).
* **Access Mechanism:** Content Providers & `Telephony` API.
* **Security Layer:** Default SMS App restrictions (introduced in Android 4.4+).

## 3. How it Works (The Logic)
The tool demonstrates the `ContentResolver.insert()` method. To modify the SMS database, the application must:
1. Request `READ_SMS` and `WRITE_SMS` permissions.
2. Be set as the **Default SMS Application** by the user.

## 4. Research Objectives
* Analyze the database schema of Android's Telephony provider.
* Demonstrate the possibility of "Local SMS Injection" for forensic study.
* Discuss mitigation strategies and digital signature verification for messages.
