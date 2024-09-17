# 🧠 Memory Forensics

This repository is a companion to my Medium article on memory forensics, which provides an introduction to analyzing system memory for uncovering potential security incidents and threats. You can read the full article [here](https://medium.com/@aashutoshlodhi/memory-forensics-7180dae80992).

## 📝 Overview

Memory forensics is a powerful technique used in digital forensics investigations. It involves capturing and analyzing volatile memory (RAM) to uncover artifacts that might not be stored on disk, such as running processes, open network connections, and loaded drivers. Memory analysis is particularly useful for:

- 🔍 Detecting malware and rootkits
- 📊 Analyzing system activity at a granular level
- 🛡️ Investigating advanced threats like fileless malware
- 💻 Understanding the state of a compromised machine

In the article, I discuss the process and tools used to perform memory forensics, focusing on frameworks like **Volatility**.

## 🔧 Tools and Techniques

The main tool discussed in the article is **Volatility**, a popular framework for memory analysis. This repository includes scripts and configurations to replicate the analysis described.

### 🛠️ Volatility Command List

Below is a list of commonly used Volatility commands that help extract various details from memory dumps:

- **Processes**:
    ```bash
    volatility pslist
    volatility pstree
    volatility psscan
    ```
- **DLL and Handles**:
    ```bash
    volatility dlllist
    volatility handles
    ```
- **Network Connections**:
    ```bash
    volatility netscan
    ```
- **Kernel Modules**:
    ```bash
    volatility modules
    volatility modscan
    ```
- **Files and Registry Hives**:
    ```bash
    volatility filescan
    volatility hivelist
    ```
- **Processes Memory Dump**:
    ```bash
    volatility procdump -p <PID> -D <output_directory>
    ```

You can find more information about how to install and use Volatility in my blog post.

## 🎯 Challenges

As part of my journey in memory forensics, I have designed several small challenges related to memory analysis. You can find these challenges in the `challenges/` directory, which includes memory dumps and specific scenarios for you to investigate using Volatility.

## 🚀 How to Use

1. Clone this repository:
    ```bash
    git clone https://github.com/yourusername/memory-forensics.git
    ```

2. Install Volatility:
    - Follow the [official Volatility documentation](https://www.volatilityfoundation.org/).

3. Explore the challenges:
    - Each challenge comes with a specific memory dump and a brief description of what to investigate.

4. Solve the challenges by analyzing the memory dumps using Volatility commands listed above.

## 🤝 Contributions

Feel free to submit pull requests or raise issues if you have any ideas, feedback, or encounter any problems!
