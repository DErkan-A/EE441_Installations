# EE441_Installations
Tutorial on how to install base requirements for the METU EE441 course

## Installing Miniconda

If you don’t have **Anaconda** or **Miniconda** installed, follow these steps to install **Miniconda**. Miniconda is a lightweight version of Anaconda that includes only `conda` and a minimal set of packages.

### Step 1: Download Miniconda

1. Go to the official [Miniconda website](https://docs.conda.io/en/latest/miniconda.html).
2. Select the installer for your operating system:
   - **Windows**: Choose the `.exe` installer.
   - **macOS**: Choose the `.pkg` installer.
   - **Linux**: Choose the `.sh` installer.
   
3. Download the installer file to your computer.

### Step 2: Install Miniconda

#### On Windows:

1. Double-click the downloaded `.exe` file to run the installer.
2. Follow the installation instructions:
   - Select "Install for Just Me" unless you want a system-wide installation.
   - Add Miniconda to your `PATH` environment variable during installation (optional).
3. After installation, search for and open the **Anaconda Prompt** or **Miniconda Prompt** from your start menu.

#### On macOS and Linux:

1. Open a terminal.
2. Navigate to the directory where you downloaded the installer and run:

```bash
bash Miniconda3-latest-MacOSX-x86_64.sh  # For macOS
bash Miniconda3-latest-Linux-x86_64.sh   # For Linux
```

# Installing GCC and GNU Make using Anaconda Prompt

This part explains how to install **GCC (GNU Compiler Collection)** and **GNU Make** using the Anaconda prompt with `conda`. These tools are essential for compiling and building C/C++ projects.

## Prerequisites

- **Anaconda/Miniconda** installed on your system.
- Basic understanding of using the command line and the Anaconda prompt.

---

## Step 1: Open Anaconda Prompt

- Open the **Anaconda Prompt** from the Start Menu or your application search bar.

---

## Step 2: Create or Activate a Conda Environment (Optional)

It’s recommended to use a separate environment for development.

### To create a new environment:

```bash
conda create --name myenv
conda activate myenv
