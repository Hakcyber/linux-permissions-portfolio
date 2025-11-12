
# 🧑‍💻 File Permissions in Linux

## 📘 Project Description
In this project, I worked as a security professional using Linux commands to ensure proper file permissions and enforce access policies.  
By using commands like `ls -la` and `chmod`, I verified, managed, and improved system security by limiting unauthorized access.  
This project demonstrates my ability to apply Linux security principles in real-world scenarios.

---

## 🔍 Check File and Directory Details
I used the `ls -l` and `ls -la` commands to list all files and their permissions, including hidden files.  
These commands helped me verify which users and groups had access, and understand how permissions were assigned to each file and directory.

```bash
ls -la /home/researcher2/project
```

Example output:
```
-rw-rw-r-- 1 researcher2 research_team 46 Nov 8 21:18 project_r.txt
```

In this example, the file `project_r.txt` is owned by the user **researcher2** and the group **research_team**.  
The user and group both have read and write permissions, while others have read-only access.

---

## 🔠 Describe the Permissions String
The permissions string `-rw-rw-r--` represents the type of file and the access rights granted to different users.

- The first symbol `-` indicates this is a regular file, not a directory.  
- The user (owner) has read and write permissions.  
- The group also has read and write permissions.  
- Other users have read-only access.

This structure ensures that access is limited based on role, supporting the **principle of least privilege**.

---

## 🔧 Change File Permissions
As a security professional, I used the `chmod` command to remove unnecessary privileges from unauthorized users.  
I applied the command:

```bash
chmod u=rw,g=rw,o=r project_r.txt
```

This change ensured that only the user and group could read and write to the file, while “others” were limited to read-only access — reducing the risk of unauthorized modification.

---

## 👁️ Change File Permissions on a Hidden File
In this step, I managed the permissions of a hidden file named `.project_x.txt`, which should not have write permissions for any user.  
Using the `chmod` command, I removed write privileges and ensured that only the user and group can read the file, while “others” have no access.

```bash
chmod u=r,g=r,o=--- .project_x.txt
```

This configuration enforces the **principle of least privilege**, ensuring archived or sensitive files remain protected from accidental or unauthorized modifications.

---

## 📁 Change Directory Permissions
In this step, I enforced the **principle of least privilege** by removing unnecessary execute permissions from the group and others.  
This ensures that only the user can access and work inside the `drafts` directory, while all other users are restricted from entering or viewing its contents.

```bash
chmod go-x drafts
```

This strengthens directory security by limiting access strictly to authorized personnel.

---

## 🧾 Summary
In this project, I reviewed and modified file and directory permissions to strengthen system security.  
By using Linux commands such as `ls -la` and `chmod`, I identified and removed unnecessary privileges to enforce the **principle of least privilege**.  
These actions ensured that only authorized users retained access, reducing the risk of unauthorized modification or exposure.
