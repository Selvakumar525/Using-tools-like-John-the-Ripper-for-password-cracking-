# Using-tools-like-John-the-Ripper-for-password-cracking
## AIM:
To crack password hashes using John the Ripper in Kali Linux.

## DESIGN STEPS:
### Step 1:
Install John the Ripper using the command:

### Step 2:
Prepare the password hash file (e.g., using unshadow for Linux password and shadow files).

### Step 3:
Use John the Ripper to crack the hashes:

## PROGRAM:

- **Install the John Ripper**
  ```bash
  sudo apt install john
  ```
- **Create a Password-Protected ZIP File**
   Archive a normal file (secret.txt) into a password-protected ZIP file
   ```bash
   zip --password 123abc secret.txt.zip secret.txt
   ```
 - **Extract the Hash from the ZIP File**
   ```bash
   zip2john secret.txt.zip > zip_hash.txt
   ```
- **Crack the ZIP Password using John**
  ```bash
  john --format=zip zip_hash.txt
  ```
- **Show the Cracked Password**
  ```bash
  john --show zip_hash.txt
  ```

## OUTPUT:
### Create a Password-Protected ZIP File
![image](https://github.com/user-attachments/assets/cdbdd837-d63b-4d00-97d8-91d1e0999dae)

### Extract the Hash from the ZIP File
![image](https://github.com/user-attachments/assets/224bf1b0-dd76-4cd1-ad93-9f2191f62607)

![image](https://github.com/user-attachments/assets/bf52a9ec-8059-44d2-93bc-35b8a8139ef9)

### Crack the ZIP Password using John
![image](https://github.com/user-attachments/assets/c2b43881-5852-4e6a-b576-7f4761e1df56)

### Show the Cracked Password
![image](https://github.com/user-attachments/assets/06b0bc3b-0aa7-4c47-9487-7b4be189a125)

## RESULT:
The password hashes were successfully cracked using John the Ripper.

