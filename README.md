# Tutorial for installing coding requirements of METU EE441 course

This tutorial will walk you through installing **GCC**, **GNU make**, and **VS Code**, all of which will be used throughout the course.
---
# Installing GCC and GNU Make using Anaconda/Miniconda Prompt

If you don’t have **Anaconda** or **Miniconda** already installed, follow these steps to install **Miniconda**. Miniconda is a lightweight version of Anaconda that includes only `conda` and a minimal set of packages. If you are comfortable and know what you are doing, you can also install GCC and GNU Make without Conda.

## Step 1: Download Miniconda

1. Go to the official [Miniconda website](https://docs.conda.io/en/latest/miniconda.html).
2. Select the installer for your operating system:
   - **Windows**: Choose the `.exe` installer.
   - **macOS**: Choose the `.pkg` installer.
   - **Linux**: Choose the `.sh` installer.
   
3. Download the installer file to your computer.
---
## Step 2: Install Miniconda

### On Windows:

1. Double-click the downloaded `.exe` file to run the installer.
2. Follow the installation instructions:
   - Select "Install for Just Me" unless you want a system-wide installation.
   - Select "Clear cache" to clean up after installation.
3. After installation, search for and open the **Anaconda Prompt** or **Miniconda Prompt** from your start menu.

### On macOS and Linux:

1. Open a terminal.
2. Navigate to the directory where you downloaded the installer and run:

```bash
bash Miniconda3-latest-MacOSX-x86_64.sh  # For macOS
bash Miniconda3-latest-Linux-x86_64.sh   # For Linux
```
3. Follow the on-screen prompts to complete the installation.
4. After installation, restart your terminal or open a new terminal window and type:
   
```bash
bash conda --version
```

This should return the installed version of Conda, indicating that Miniconda is installed correctly.

---
## Step 3: Open Anaconda/Miniconda Prompt
- Open the **Anaconda Prompt** from the Start Menu or your application search bar.
- On Linux/macOS, open a terminal window.
---
## Step 4: Create or Activate a Conda Environment (Optional)
For this course  you do not need to create an environment, but it’s generally recommended to use a separate environment for development tasks.
### To create a new environment:

```bash
conda create --name myenv
```
- Replace `myenv` with your preferred environment name.
### To activate an existing environment:

```bash
conda activate myenv
```
---
## Step 5: Install GCC and GNU Make
Now, install **GCC** and **GNU Make** based on your operating system.
### Installing GCC:

#### On Windows:
```bash
conda install -c msys2 m2w64-gcc
```
#### On macOS:
```bash
conda install -c conda-forge clang_osx-64
```

#### On Linux:
```bash
conda install -c conda-forge gcc_linux-64
```

### Installing GNU Make:
```bash
conda install -c conda-forge make
```
---
## Step 6: Verify the Installation
To confirm that GCC and GNU Make have been installed successfully, run the following commands:

```bash
gcc --version
make --version
```
You should see the version information for both GCC and GNU Make.

# Installing Visual Studio Code (VS Code)

This part of the guide will walk you through the steps to install **Visual Studio Code (VS Code)**, a lightweight, powerful code editor developed by Microsoft. VS Code supports multiple programming languages, has a rich extension ecosystem, and is an excellent tool for coding.

---

## Step 1: Download Visual Studio Code

To begin, download the Visual Studio Code installer for your operating system.

1. Go to the official [Visual Studio Code website](https://code.visualstudio.com/).
2. Choose the correct version for your platform:
   - **Windows**: `.exe` installer.
   - **macOS**: `.zip` or `.dmg` installer.
   - **Linux**: `.deb` or `.rpm` package, or download via Snap.

---

## Step 2: Install Visual Studio Code

### For Windows:

1. Run the `.exe` installer that you downloaded.
2. Accept the license agreement.
3. Choose the destination folder for installation.
4. (Optional) Select additional tasks such as:
   - Creating a desktop icon.
   - Adding VS Code to your `PATH` (recommended for command-line access).
   - Associating VS Code with common file types such as `.html`, `.js`, `.py`, etc.
5. Click **Install** and wait for the installation to complete.
6. Once installed, launch Visual Studio Code from the Start menu or desktop.

### For macOS:

1. Open the `.dmg` file.
2. Drag the Visual Studio Code application to your **Applications** folder.
3. You can now launch Visual Studio Code from the **Applications** folder or search for it via **Spotlight**.
4. (Optional) To add VS Code to your command-line tools, open VS Code, press `Cmd` + `Shift` + `P`, type `Shell Command: Install 'code' command in PATH`, and press Enter.

### For Debian and Ubuntu-based distributions:

1. Open a terminal and run the following command to install the `.deb` package:
```bash
sudo apt install ./<file>.deb
```
2. Replace `<file>` with the name of the `.deb` file you downloaded.
---
## Step 3:  Verify the Installation
To verify that VS Code is correctly installed, follow these steps:
1. Launch VS Code:
   - On **Windows**, use the Start menu.
   - On **macOS**, use the Applications folder or Spotlight search.
   - On **Linux**, use your app launcher or run `code` from the terminal.
2. Once VS Code is open, you should see the welcome screen. You can now start coding!
---
## Step 4:  Customize VS Code (Optional)
Visual Studio Code has a wide variety of extensions and themes available for different languages and workflows. You can install these directly from the **Extensions** marketplace:
### To install an extension:
1. Open VS Code.
2. Click on the **Extensions** icon in the Activity Bar on the left (or press `Ctrl` + `Shift` + `X`).
3. Search for the extension you want (e.g., Python, JavaScript, etc.).
4. Click **Install** to add the extension to your editor.

---
# Additional Resources

Below are useful resources and documentation for learning more about **Anaconda**, **GCC**, and **GNU Make**.

## Anaconda/Miniconda Documentation

- [Anaconda Documentation](https://docs.anaconda.com/): Official documentation for Anaconda, including guides on installation, using conda environments, and package management.
- [Miniconda Documentation](https://docs.conda.io/en/latest/miniconda.html): Official documentation for Miniconda, a lightweight version of Anaconda, which includes the `conda` package manager.

## Conda-forge

- [Conda-forge](https://conda-forge.org/): A community-led collection of recipes, build infrastructure, and distributions for the conda package manager. You can find thousands of packages available through conda-forge.

## GCC (GNU Compiler Collection)

- [GNU GCC](https://gcc.gnu.org/): Official site for GCC, which includes documentation, installation instructions, and details about the compiler's features.
- [GCC Manual](https://gcc.gnu.org/onlinedocs/): Comprehensive manual for the GCC compiler. Includes detailed documentation for compiling programs in various languages supported by GCC.

## GNU Make

- [GNU Make](https://www.gnu.org/software/make/): Official site for GNU Make, which automates the build process of projects. This site includes a download link and basic documentation.
- [GNU Make Manual](https://www.gnu.org/software/make/manual/make.html): The official GNU Make manual, covering how to write `Makefile` scripts and use Make effectively for building projects.

## VS Code

- [VS Code Official Documentation](https://code.visualstudio.com/docs): he official documentation covering setup, extensions, and using Visual Studio Code.
---

Feel free to explore these resources for further learning and troubleshooting! Remember that you can always ask your TAs for help with anything you cannot do yourself in a reasonable time frame.
