# Oracle Key Vault (OKV) - SSH Key Management

In **Lab 3** you will confirm that unmanaged SSH public key authentication allows you to login to a remote server (dbseclab) from your workstation (db26ai) without knowing the remote server password. 

*Estimated Lab Time:* 3 minutes

## Task 1: Get to know your Environment

- Click on each Remote Desktop link available in the Labs details to open web browser tabs for each of them.

- **Remote SSH Server** desktop (here `dbsec-lab` with Private IP `10.0.0.150`)

    ![Key Vault](./images/okv_ssh-001.png "Remote SSH Server")

    **Note**: This tab will be your main workspace throughout the lab.

- **SSH Client workstation** (here `db26ai` with Private IP `10.0.0.155`)

    ![Key Vault](./images/okv_ssh-002.png "Admin workstation")
         
      **Note**: If you are using a remote desktop session, click on *Activities* (top left corner of the desktop), then click on the *Terminal* icon to launch a session.

## Task 2: Confirm public key authentication is working

**In this lab**, you confirm that unmanaged, file-based public key authentication from an admin workstation (db26ai) to a remote server (dbsec-lab) is working:

- On the **SSH Client workstation** (on db26ai):

- Switch to user *opc*

    ```
    <copy>
    sudo su - opc
    </copy>
    ```

- Make sure you have access to SSH Server (DBSeclab VM) *as opc*

    ```
    <copy>
    ssh opc@10.0.0.150
    </copy>
    ```

![Key Vault](./images/okv_ssh-004.png "SSH Client VM access to SSH Server VM")

**Note**: You must be successfully connected to dbsec-lab VM!

- If so, close the SSH session:

    ```
    <copy>
    exit
    </copy>
    ```

- You confirmed that SSH public key authentication is configured, allowing passwordless access from workstation db26ai to remote server dbsec-lab.