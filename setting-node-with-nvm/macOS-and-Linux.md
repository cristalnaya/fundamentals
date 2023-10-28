# Setting Up Node.js with NVM on macOS and Linux

Node.js is a JavaScript runtime that lets you run JavaScript code outside of the browser. NVM (Node Version Manager) is a utility that simplifies the management of multiple versions of Node.js on a single machine.

## Advantages of NVM:

1. **Multiple Versions:** Easily switch between Node.js versions for different projects.
2. **Isolation:** Avoids potential conflicts with system-wide Node.js installations.
3. **Simple Upgrades:** Quickly upgrade to newer Node.js versions when necessary.

## Installation

* **Using curl:**
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

* **Or, using wget:**
   ```bash
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.38.0/install.sh | bash

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

## Wrapping Up
With NVM on macOS and Linux, handling multiple versions of Node.js becomes a breeze. It provides flexibility and minimizes version-related issues.
 

