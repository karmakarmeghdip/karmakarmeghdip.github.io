### 1. **What is FTP and how is it used for file transfer?**

**File Transfer Protocol (FTP)** is a standard network protocol used to transfer files between a client and a server over a TCP/IP network, such as the internet or a local network. FTP operates on the **application layer** (Layer 7) of the OSI model and uses **port 21** by default for command control and **port 20** for data transfer in active mode.

FTP is widely used for:

- Uploading files from a local system to a remote server.
- Downloading files from a server to a local system.
- Managing files on a remote server, such as renaming, deleting, or creating directories.

**How FTP Works:**

1. A client establishes a connection to an FTP server using an FTP client application (e.g., FileZilla, WinSCP, or command-line tools).
2. The user logs in with a username and password, or anonymously in some cases.
3. After authentication, the user can send FTP commands to upload, download, or manage files on the server.
4. FTP uses separate channels for control (commands) and data (file transfer):
    - The **control channel** remains open throughout the session for commands and responses.
    - The **data channel** is established only during file transfers.

---

### 2. **What is the difference between active and passive FTP?**

FTP can operate in two modes: **active** and **passive**, which determine how the data channel is established between the client and the server.

#### **Active FTP:**

- The client connects to the server's port 21 to establish the control channel.
- The client sends its own IP address and a random port number to the server, indicating where it will listen for incoming data.
- The server initiates the data connection by opening a connection from its **port 20** to the client's specified port.
- **Challenges:**
    - Active FTP may face issues with firewalls or NAT (Network Address Translation) because the client needs to allow incoming connections from the server.

#### **Passive FTP:**

- The client connects to the server's port 21 to establish the control channel.
- Instead of the server initiating the data connection, the server sends its IP address and a port number for the client to connect to.
- The client then establishes the data connection to the server's specified port.
- **Advantages:**
    - Passive FTP works better with firewalls and NAT because the client initiates both control and data connections, avoiding the need to allow incoming server-initiated connections.

**Key Differences:**

|Feature|Active FTP|Passive FTP|
|---|---|---|
|Data Channel|Initiated by the server|Initiated by the client|
|Firewall Issues|More likely|Less likely|
|Server Port Used|Port 20|Random port specified by server|

---

### 3. **What are the common FTP commands?**

FTP supports a set of standardized commands that allow clients to interact with servers. Here are some of the most commonly used commands:

#### **Authentication and Session Management:**

- **USER:** Sends the username to the server for login.
    - Example: `USER admin`
- **PASS:** Sends the password to the server for login.
    - Example: `PASS password123`
- **QUIT:** Ends the FTP session and disconnects from the server.
    - Example: `QUIT`

#### **File Management:**

- **LIST:** Lists the files and directories in the current directory on the server.
    - Example: `LIST`
- **RETR:** Downloads a file from the server to the client.
    - Example: `RETR file.txt`
- **STOR:** Uploads a file from the client to the server.
    - Example: `STOR file.txt`
- **DELE:** Deletes a file on the server.
    - Example: `DELE file.txt`
- **RNFR:** Renames a file (specify the current name first).
    - Example: `RNFR oldfile.txt`
- **RNTO:** Renames a file (specify the new name).
    - Example: `RNTO newfile.txt`

#### **Directory Management:**

- **PWD:** Prints the current working directory on the server.
    - Example: `PWD`
- **CWD:** Changes the current working directory on the server.
    - Example: `CWD /folder`
- **MKD:** Creates a new directory on the server.
    - Example: `MKD /newfolder`
- **RMD:** Removes a directory on the server.
    - Example: `RMD /oldfolder`

#### **Connection and Transfer Settings:**

- **PORT:** Specifies the client-side port for active mode FTP.
    - Example: `PORT 192,168,1,10,12,34`
- **PASV:** Requests the server to enter passive mode.
    - Example: `PASV`
- **TYPE:** Sets the file transfer type (ASCII or binary).
    - Example: `TYPE I` (for binary)

These commands, when combined with an FTP client or used manually, provide complete control over file transfer and management operations.