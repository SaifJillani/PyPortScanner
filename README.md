# PyPortScanner
A multithreaded TCP port scanner in Python that scans IPs/domains, retrieves service banners, and detects common vulnerabilities.

# Port Scanner

A simple Python-based TCP port scanner that allows you to scan one or more target IP addresses or domain names for open ports within a specified range. This tool retrieves service banners and helps identify potential vulnerabilities.

---

## Table of Contents

- [Features](#features)  
- [Tech Stack](#tech-stack)  
- [Getting Started](#getting-started)  
  - [Prerequisites](#prerequisites)  
  - [Installation](#installation)  
- [Usage](#usage)  
  - [Options](#options)  
  - [Examples](#examples)  
- [Purpose](#purpose)

---

## Features

- Scan one or more target IP addresses or domain names.
- Specify a custom port range or scan all ports.
- Retrieve service banners and versions for open ports.
- Detect known vulnerabilities for services (e.g., FTP, SSH).
- Multithreaded scanning for faster results.
- Save scan results to a JSON file.
- Optional verbose output.

---

## Tech Stack

This project is built using the following technologies and libraries:

- Python 3.x – Core programming language  
- `argparse` – Command-line argument parsing  
- `socket` – Low-level network programming  
- `threading` – Multithreading support  
- `json` – Reading and writing JSON data  
- `tqdm` – Displaying progress bars  
- `termcolor` – Terminal output coloring  
- `IPython` – Optional for interactive use

---

## Getting Started

### Prerequisites

- Python 3.x  
- `pip` (Python package manager)

### Installation

Clone the repository:

```bash
git clone https://github.com/pannagkumaar/PortScanner.git
```

Navigate to the project directory:

```bash
cd PortScanner
```

Install the required Python packages:

```bash
pip install -r requirements.txt
```

---

## Usage

```bash
python port_scanner.py -t <targets> [-p <port-range>] [-T <timeout>] [-n <num-threads>] [-o <output>] [-v]
```

### Options

| Option               | Description                                                                |
|----------------------|----------------------------------------------------------------------------|
| `-t`, `--targets`     | Specify target IP addresses or domain names (required).                  |
| `-p`, `--port-range`  | Specify port range (e.g., `1-100` or `all`). Default is `1-100`.         |
| `-T`, `--timeout`     | Timeout value in seconds. Default is `1.0`.                              |
| `-n`, `--num-threads` | Number of threads for scanning. Default is `10`.                         |
| `-o`, `--output`      | Output file to save results (e.g., `results.json`).                      |
| `-v`, `--verbose`     | Enable verbose output.                                                   |

---

## Examples

Scan a single target with the default port range:

```bash
python port_scanner.py -t 192.168.1.1
```

Scan multiple targets with full port range and save results to a file:

```bash
python port_scanner.py -t example.com 192.168.1.1 -p 1-65535 -o results.json
```

Enable verbose mode:

```bash
python port_scanner.py -t 192.168.1.1 -v
```

---

## Purpose

This project provides a simple, effective, and extensible TCP port scanning tool for:

- Network administrators analyzing infrastructure  
- Security professionals auditing services  
- Enthusiasts learning network and security concepts

By identifying open ports and collecting service information, the scanner helps uncover misconfigurations and potential vulnerabilities.

