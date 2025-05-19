# 🔐 Linux Security Audit – Simulated Project

## Overview
As part of the Google Cybersecurity Certificate, I conducted a file and directory permission audit in a simulated corporate
environment. The goal was to align file access with security policy by restricting unauthorized write or execute access.

---

## 🔎 Objectives
- Analyze file and directory permissions in a target directory using `ls -la`
- Understand and interpret permission strings
- Apply least privilege principle to sensitive files and folders
- Use `chmod` to enforce correct access controls

---

## 🗂️ Key Tasks Performed

### ✅ 1. Checked File & Directory Details
Used:
```bash
ls -la ~/projects

Reviewed file types, owners, and permission sets.
Identified files needing permission corrections (e.g. project_k.txt, .project_x.txt, drafts/).

### ✅ 2. Interpreted Permission Strings
Example:

cpp
Copy
Edit
-rw-rw-r--  project_t.txt
- : Regular file

rw- : User has read/write

rw- : Group has read/write

r-- : Others can only read

### ✅ 3. Modified File Permissions
🔧 Remove write permission from "others" for project_k.txt:
bash
Copy
Edit
chmod o-w project_k.txt
🔧 Update .project_x.txt (hidden file):
bash
Copy
Edit
chmod u-w .project_x.txt
chmod g-w .project_x.txt
chmod g+r .project_x.txt
No write permissions for user or group.

Group can only read.

Others have no access.

### ✅ 4. Secured Directory Access (drafts/)
Goal: Only researcher2 should have execute (access) rights.

bash
Copy
Edit
chmod g-x drafts/
Removed execute permission for group.

Ensured only researcher2 retained execute access to the drafts directory.

### 🛠️ Tools Used
ls -la

chmod

Linux terminal (Ubuntu CLI)

📚 What I Learned
How to read, interpret, and correct Linux file permission strings.

When and why to apply least privilege to files.

Safe use of chmod in multi-user environments.

Importance of directory execute permissions for access control.



"In cybersecurity, the smallest permission misconfiguration can open the biggest hole."
