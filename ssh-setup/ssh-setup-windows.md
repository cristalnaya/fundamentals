# Setting Up SSH on Windows Using Git Bash

SSH (Secure Socket SHell) is a protocol that allows secure remote login and other secure network services over an insecure network. This guide explains how to set up SSH keys on a Windows machine using Git Bash.

## Using Git Bash

1. **Open Git Bash**: You can search for it from the Start menu.
2. Check for Existing SSH Keys:
```bash
ls -al ~/.ssh
```

3. **Generate SSH Key**: Run the following command, replacing the email with the email address associated with your GitHub account:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

4. Start the ssh-agent in the background:
```bash
eval $(ssh-agent -s) 
```

5. Add the SSH Key to the ssh-agent:
```bash
ssh-add ~/.ssh/id_ed25519
```

## Adding the SSH Key to GitHub:
1. Copy the SSH Key to Clipboard: In Git Bash, use:
```bash
cat ~/.ssh/id_ed25519.pub | clip
```
2. **Add SSH Key to GitHub:**
   * Navigate to GitHub and log into your account.
   * Click on your profile picture in the top right corner and select **Settings**.
   * On the left sidebar, click on **SSH and GPG keys**.
   * Click the **New SSH key** button.
   * Paste your copied SSH key into the "Key" field.
   * Provide a descriptive title for the "Title" field.
   * Click **Add SSH key**.
   
## Testing the Connection:
1. In Git Bash, run:
```bash
ssh -T git@github.com
```
2. You might see a warning about authenticity. If so, type `yes` and press **Enter**.
3. If set up correctly, you'll receive a message saying you've successfully authenticated.

## Conclusion:
By following these steps, you have successfully set up an SSH key on Windows using Git Bash. This ensures a secure connection to remote repositories without entering credentials every time.
