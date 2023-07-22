# Windows dev environment setup

## 🚀 Overview

Setting up a development environment on Windows can be a challenging task, but with the right tools and guidance, it can be made easier. This guide will provide step-by-step instructions for setting up a development environment on Windows, including installing WSL, Terminal, Git, and Visual Studio Code Insider.

### Prerequisites:

Before beginning the setup process, ensure that your system meets the following requirements:

- Windows 10 version 1903 or higher
- Administrator access to your machine
- An internet connection

## 🐧 WSL: The Heart of Your Windows Dev Environment

To set up your Windows development environment, the first and most vital step is installing the Windows Subsystem for Linux (WSL). 🚀
### 💻 Installing WSL 2: A Breeze

WSL 2 is the latest version, featuring a full Linux kernel and complete system call compatibility. No longer requiring multiple steps, all you need to do is execute this single command in PowerShell or Command Prompt:

```sh
wsl --install
```

This command accomplishes the following:

- Enables the optional WSL and Virtual Machine Platform components
- Downloads and installs the latest Linux kernel
- Sets WSL 2 as the default
- Downloads and installs the Ubuntu Linux distribution (a reboot may be required)

Should you wish to change your default Linux distribution, follow the provided [documentation](https://docs.microsoft.com/en-us/windows/wsl/install#change-the-default-Linux-distribution-installed). 📚

With WSL at your disposal, the Windows development landscape becomes yours to conquer! 💪🌟

### 🔧 **Setting Up Linux User & Password:**

🔒 After installing your Linux distribution with WSL, launch it from the Start menu. You'll create a unique User Name and Password during the initial run.

💡 These credentials are specific to each Linux distribution and don't relate to your Windows user.

⚠️ Password entry is blind typing, normal behavior, nothing will show on the screen.

👤 Your account becomes the default user and auto-signs in on launch.

📝 Each WSL distribution has its own set of user accounts. Configuring a new account is necessary when adding, reinstalling, or resetting.

### 📦 **Update & Upgrade Packages:**

To keep your system shipshape, regularly update and upgrade packages with your distribution's preferred package manager. For Ubuntu or Debian, execute:

```bash
sudo apt update && sudo apt upgrade
```

⚙️ Windows won't auto-update or upgrade your Linux distribution(s). Linux users typically prefer controlling this task themselves.

## ⌨️ **Set Up Windows Terminal: Power Up Your Command Line**

<img src="img/terminal.png" alt="Microsoft Terminal" />

Windows Terminal unleashes the potential of any application with a command line interface.

🐧 Whenever a new WSL Linux distribution is installed, Windows Terminal conjures a dedicated instance that you can fine-tune to your liking.

💡Head to the Windows Terminal docs for setup and personalization assistance. Customize:

1. Installation: Get it from the Microsoft Store - [Windows Terminal or Windows Terminal (Preview)](https://learn.microsoft.com/en-us/windows/terminal/get-started).
2. Custom Actions: [Set up keyboard shortcuts that suit your natural workflow](https://learn.microsoft.com/en-us/windows/terminal/#custom-actions).
3. Default Startup Profile: Configure your preferred starting setup.
   1. Select the ˅ icon from Windows Terminal and go to the Settings menu
   2. Startup section find the Default profile dropdown, select Ubuntu and Windows Terminal as the Default terminal
5. Appearance: Tailor [themes](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/appearance#theme), [color schemes](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/color-schemes), [names, starting directories](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/profile-general), [background images](https://learn.microsoft.com/en-us/windows/terminal/customize-settings/profile-appearance#background-image), and more...
6. Set up a custom prompt for [PowerShell or WSL with Oh My Posh](https://learn.microsoft.com/en-us/windows/terminal/tutorials/custom-prompt-setup).

## 📝💻 **Set Up Your Favorite Code Editor**

👉 Recommended Visual Studio Code Insiders for seamless remote development and debugging with WSL.

🚀 **Use Visual Studio Code Insiders:**

Follow these steps to get started:

1. Install [Visual Studio Code insiders](https://code.visualstudio.com/insiders/).
2. Get the [Remote Development extension pack for WSL](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.vscode-remote-extensionpack).
3. [Follow this step-by-step guide to Get started using Visual Studio Code with WSL](https://learn.microsoft.com/en-us/windows/wsl/tutorials/wsl-vscode).

<img src="img/vscode-remote-wsl-extensions.png" alt="Microsoft VS Code" />

Once set up, open your WSL project with a VS Code remote server:

```bash
code-insiders .
```

Don't forget the period at the end to open the current directory. 💫💡
