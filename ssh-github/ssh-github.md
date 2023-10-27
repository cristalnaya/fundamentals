# SSH Keys and GitHub
## Introduction
SSH (Secure Shell) keys offer a secure method for connecting to GitHub without the need to enter your username and password each time. By setting up an SSH key and adding it to your GitHub account, you can push, pull, and interact with repositories securely.

## Generating an SSH Key
1. **Open Terminal:** This can be your operating system's terminal or command line interface.
2. **Generate SSH Key:** Run the following command, replacing the email with the email address associated with your GitHub account:

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```
* You'll be asked where you want to save your key. Press Enter to accept the default location.
* Next, you'll be prompted to enter a passphrase. This is an optional, additional layer of security.
3. Ensure the ssh-agent is running:

```bash
eval "$(ssh-agent -s)"
```
4. Add the SSH Key to the ssh-agent:

```bash
ssh-add ~/.ssh/id_ed25519
```

## Adding the SSH Key to GitHub
1. Copy the SSH Key to Clipboard: You'll need to install xclip if you're on Linux. If you're on Mac, pbcopy is pre-installed.

* **For Mac:**

```bash
pbcopy < ~/.ssh/id_ed25519.pub
```
* **For Linux (installing xclip and copying):**

```bash
sudo apt-get install xclip
xclip -sel clip < ~/.ssh/id_ed25519.pub
```

2. Add SSH Key to GitHub:
* Go to GitHub and log into your account.
* Click on your profile picture in the top right corner and go to Settings.
* In the left sidebar, click on SSH and GPG keys.
* Click on the New SSH key button.
* Paste your copied SSH key into the "Key" field.
* Give your key a descriptive title in the "Title" field.
* Click on Add SSH key.

## Testing the Connection
1. Run the following command:

```bash
ssh -T git@github.com
```

2. You might see a warning about authenticity. Type yes and press Enter.
3. If everything is set up correctly, you'll see a message saying you've successfully authenticated.

## Conclusion
You've now set up an SSH key for your machine and added it to GitHub. This provides a secure method of interacting with your GitHub repositories without needing to input your credentials each time.
