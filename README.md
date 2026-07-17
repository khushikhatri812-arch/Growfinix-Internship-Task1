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

```
## Phase 2: Threat Intelligence & Asset Detection (Shodan)

###  Objective
The goal of this phase was to use Shodan as an internet-wide intelligence engine to discover open services, network mappings, and infrastructure details for the target domain without running an active, disruptive network port scan.

### 🛠️ Installation & Troubleshooting
During the installation on Python 3.14, a ModuleNotFoundError occurred regarding a missing pkg_resources module. This was fixed by installing a compatible version of the core setup tools:

```powershell
# Fixed the dependency environment
pip install setuptools==81.0.0

# Installed the Shodan CLI package
pip install -U shodan

# Linked the terminal using the unique Shodan API Key
shodan init <YOUR_API_KEY_HERE>

# Phase 3: Data Link Analysis & Visual Reconnaissance (Maltego)

### 🔍 Objective
The objective of this phase was to aggregate the discovered target infrastructure into a unified visual intelligence graph, analyzing the relationships between the root domain and its child assets to understand the overall attack surface map.

### 🛠️ Configuration & Workflow
1. Launched *Maltego Community Edition (CE)* and created a blank workspace graph.
2. Dragged a *Domain Infrastructure Entity* onto the grid and targeted owasp.org.
3. Executed the [Utilities] To DNS Name [Using Name Schema dictionary] transform from the *DNS from Domain* suite.

<img width="960" height="504" alt="Screenshot 2026-07-17 150324" src="https://github.com/user-attachments/assets/33a173c9-cd0c-4b25-be9e-3ce2119ee934" />
<img width="960" height="504" alt="Screenshot 2026-07-17 152222" src="https://github.com/user-attachments/assets/0ada27fd-0c98-43f5-9857-b644c8839b0d" />
<img width="960" height="540" alt="Screenshot 2026-07-17 152158" src="https://github.com/user-attachments/assets/a32044c6-bb60-43eb-8383-a0dd728f02b1" />
<img width="960" height="504" alt="Screenshot 2026-07-17 152046" src="https://github.com/user-attachments/assets/aab254e6-699a-4c43-b5a4-90fbed0bd56b" />
<img width="960" height="504" alt="Screenshot 2026-07-17 150255" src="https://github.com/user-attachments/assets/9e23ff39-9b5f-4607-9b6e-a9b4eb4a2d2a" />
<img width="960" height="504" alt="Screenshot 2026-07-17 150244" src="https://github.com/user-attachments/assets/5a7141b6-99ec-498c-8f41-cf559e3d0ea9" />
<img width="960" height="504" alt="Screenshot 2026-07-17 145904" src="https://github.com/user-attachments/assets/1978160d-5b10-4bb8-a548-cd1ad47c6108" />



### 📊 Visual Intelligence Discovered
The transform successfully mapped out relationships to major structural endpoints, revealing direct architectural dependencies:
*   admin.owasp.org
*   cloud.owasp.org
*   groups.owasp.org
*   mail.owasp.org
*   www.owasp.org



