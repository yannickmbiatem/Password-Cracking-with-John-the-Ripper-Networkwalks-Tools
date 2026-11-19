# Password-Cracking-with-John-the-Ripper-Networkwalks-Tools

## 📌 Project Overview
This repository contains the documentation and practical work for **Week 3** of the Cybersecurity & Ethical Hacking program at **Networkwalks (Batch B084)**. 

The objective of this project was to understand the mechanics of password cracking by extracting hashes from password-protected PDF files and recovering the passwords using both industry-standard tools and custom web-based tools.

**Modules Covered:**
*   **W3-PM1:** Password Cracking with John the Ripper (JTR) & Johnny GUI
*   **W3-PM2:** Password Cracking with Networkwalks Online Tools

---

## ⚠️ Disclaimer
These activities were performed in a controlled, educational lab environment using provided files where I had explicit permission to test. This documentation is for educational and research purposes only. Do not use these techniques on systems or files you do not own or have written permission to test. Unauthorized access is illegal.

---

## 🛠️ Tools Used
*   **John the Ripper (JTR):** Command-line password cracking tool.
*   **Johnny GUI:** Graphical interface for John the Ripper.
*   **OnlineHashCrack:** Web tool used to extract the hash from the PDF file.
*   **Networkwalks Hash Calculator:** Custom tool to extract hashes from protected PDFs.
*   **Networkwalks Password Cracker:** Custom tool to crack hashes via a web browser.
*   **Windows OS:** Environment used for the lab.

---

## 🚀 Lab Execution & Walkthrough

### Part 1: Password Cracking with John the Ripper (W3-PM1)

#### Step 1: Installation and Setup
I downloaded and installed John the Ripper (JTR) and the Johnny GUI on my Windows machine. After installation, I configured Johnny by browsing to the `john.exe` executable file located in the JTR installation folder (`run` directory).

![Johnny Settings](YOUR_IMAGE_LINK_HERE)

#### Step 2: Hash Extraction
To crack the password, the first step is to extract the hash from the locked PDF (`My Locked PDF1.pdf`). I used the OnlineHashCrack PDF Hash Extractor tool, uploaded the PDF, and copied the resulting `$pdf$...` hash value.

![Hash Extraction](YOUR_IMAGE_LINK_HERE)

#### Step 3: Preparing the Hash File
I opened Notepad, pasted the extracted hash, and saved the file as `hash1.txt`. 
*(Note: I ensured the hash started exactly with `$pdf$` and removed any extra formatting characters).*

![Notepad Hash File](YOUR_IMAGE_LINK_HERE)

#### Step 4: Cracking with Johnny
I opened Johnny, loaded the `hash1.txt` file, and clicked **"Start new attack."** The tool successfully processed the hash and recovered the password: `password1`.

![Johnny Cracked](YOUR_IMAGE_LINK_HERE)

#### Step 5: Verification
I opened the encrypted PDF file, entered the recovered password (`password1`), and successfully unlocked the document, revealing the "Congratulations" flag.

![Unlocked PDF](YOUR_IMAGE_LINK_HERE)

---

### Part 2: Password Cracking with Networkwalks Tools (W3-PM2)

#### Step 1: Using the Hash Calculator
I navigated to the Networkwalks Hash Calculator web tool. I uploaded the same `My Locked PDF1.pdf` file. The tool automatically parsed the file and extracted the crackable hash.

![NW Hash Calculator](YOUR_IMAGE_LINK_HERE)

#### Step 2: Using the Password Cracker
I copied the extracted hash and navigated to the Networkwalks Password Cracker web tool. I pasted the hash into the input field and initiated the cracking process. 

![NW Password Cracker](YOUR_IMAGE_LINK_HERE)

#### Step 3: Successful Crack
The web-based tool successfully processed the hash and revealed the password: `password1`.

![NW Cracked Success](YOUR_IMAGE_LINK_HERE)

---

## 💡 Key Learnings & Takeaways

1.  **Encryption vs. Hashing:** I learned that encryption is a two-way function (data can be decrypted with a key), whereas hashing is a one-way function (scrambling data into a fixed-size digest). Password cracking involves trying to find the plaintext that matches a specific hash.
2.  **Tool Flexibility:** I gained experience using both a traditional command-line tool (JTR/Johnny) and modern, browser-based tools (Networkwalks). 
3.  **Password Security:** This exercise demonstrated how quickly weak or common passwords (like `password1`) can be cracked using dictionary attacks. It reinforces the absolute necessity of using complex, long, and unique passwords for sensitive files and systems.

---
**Author:** Yannick Mbiatem  
**Program:** Cybersecurity Intern B084  
**Institution:** Networkwalks  
**Instructor:** Waqas Karim (CCIE)
