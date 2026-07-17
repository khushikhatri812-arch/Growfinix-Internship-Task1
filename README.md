# Growfinix Technology Internship - Cybersecurity Tasks

This repository contains the practical tasks completed during my Cybersecurity Internship at *Growfinix Technology*. It demonstrates core concepts of (OSINT), passive reconnaissance, and threat reporting.

---

## Task 1: Passive Reconnaissance & Information Gathering

###  Project Overview
The objective of this task was to perform passive reconnaissance on a target domain to discover publicly available information—such as subdomains, hosts, and email addresses—without directly interacting with the target's infrastructure. This mimics the initial phase an attacker or a penetration tester goes through during a security assessment.

###  Tech Stack & Tools Used
*   *Operating System:* Windows 11 (PowerShell)
*   *Language Environment:* Python 3.14
*   *Primary Tool:* theHarvester (v4.11.1)
*   *Search Configurations:* DuckDuckGo, CRTsh

---

##  Setup and Installation

Because the latest repository structure uses modern package management (pyproject.toml and uv.lock), the traditional requirements.txt approach was bypassed. The tool was successfully built and installed globally within the environment using:

```powershell
# Navigate to the project directory
cd .\theHarvester-master\theHarvester-master\

# Install the application and its local dependencies
pip install .
