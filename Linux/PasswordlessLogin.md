# Passwordless Login using SSH

*[Home](linux.md)*
#### Step 0: Login to the Server

```
ssh root@134.122.120.216
```
This time it asks for password (We assume there is no prior configuration for passwordless login)

#### Step 1: Make public/private key pair
Generate the key pair in the source system
```
ssh-keygen -t rsa
```
Don't give any passphrase, As we want to connect to the server without password or passphrase. This command generates two files, one is private key which is id_rsa and public key id_rsa.pub under the directory /root/.ssh
```
cd /root/.ssh
ls -ltra
```
Verify the two files id_rsa and id_rsa.pub under the folder /root/.ssh

#### Step 2.0 Copy Public key to the Server
This can be done by two ways. By using ssh-copy-id command or manually copying the key to the server.
```
ssh-copy-id root@134.122.120.216
```
The above command copies the public key from /root/.ssh/id_rsa.pub to the /root/.ssh/authorized_keys.

#### Step 2.1 Manually Copy the Public key
If we implemented the step 2.0 we can ignore this step.
```
cat /root/.ssh/id_rsa
```
Copy the printed text on the console<br/>
Connect to the Server
```
ssh root@134.122.120.216
```
Edit the file /root/.ssh/authorized_keys file using any file editor. Paste the copied public key and save the file
```
vi /root/.ssh/authorized_keys
```
The security permissions for .ssh folder is (700) and security permissions for file authorized_keys is (600).
#### Step 3: Verify the login
```
ssh root@134.122.120.216
```
This time it doesn't ask for the password
#### Step 4: Disable password logins for the server
Edit  file /etc/ssh/sshd_config file and restart sshd.
```
vi /etc/ssh/sshd_config
```
Set the following properties to no
```
PasswordAuthentication no
ChallengeResponseAuthentication no
UsePAM no
```
Restart sshd
```
systemctl restart sshd
```
#### Step 4.0 Try to login to server using another user.
```
ssh ravi@134.122.120.216
```
Output shows as Permission denied and does not ask for password also.<br/>
Since we configured the passwordless login for the user root and disabled the password logins We cannot connect to server using ravi user.

*[Home](linux.md)*
