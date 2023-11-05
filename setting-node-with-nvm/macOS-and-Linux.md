# Setting Up Node.js with NVM on macOS and Linux

Node.js is a JavaScript runtime that lets you run JavaScript code outside the browser. NVM (Node Version Manager) is a utility that simplifies the management of multiple versions of Node.js on a single machine.

## Advantages of NVM:

1. **Multiple Versions:** Easily switch between Node.js versions for different projects.
2. **Isolation:** Avoids potential conflicts with system-wide Node.js installations.
3. **Simple Upgrades:** Quickly upgrade to newer Node.js versions when necessary.

## Installation

* **Using curl:**
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash

* **Or, using wget:**
   ```bash
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.5/install.sh | bash
  
## Verification
Check the installed NVM version:
 ```bash
nvm -v
```

## Usage

1. List available versions:
    ```bash
   nvm ls-remote

2. Install a specific version
    ```bash
   nvm install <version>

3. Switch to an installed version:
    ```bash
   nvm use <version>

4. Set a default version:
    ```bash
   nvm alias default <version>

**Note:** It's a good practice to visit the [official nvm GitHub repository](https://github.com/nvm-sh/nvm#installing-and-updating) to check for the latest stable release version and use the corresponding installation command from there.
## Wrapping Up
With NVM on macOS and Linux, handling multiple versions of Node.js becomes a breeze. It provides flexibility and minimizes version-related issues.

## Additional guide:
To install `curl` or `wget` on a Mac, you typically use a package manager like Homebrew, which is widely regarded as the preferred package manager for macOS.

### Installing Homebrew:
If Homebrew is not installed on your Mac, you can install it first. Open the Terminal app and run the following command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This script will explain what it will do and then pause before it does it. There are more installation options available (needed for macOS on ARM, for instance), which you can review on the Homebrew website.

### Installing curl:
`curl` is typically installed by default on macOS, but if you need to install or update it, you can do so using Homebrew:

```sh
brew install curl
```
This will download and install the latest version of curl.

### Installing wget:
To install `wget`, you can use Homebrew with the following command:

```sh
brew install wget
```
After running the installation command, you can verify the installation by checking the version of `curl` or `wget`:

```sh
curl --version
```
or

```sh
wget --version
```
These commands should return the version of `curl` or `wget` that you installed, confirming that the installation was successful.
