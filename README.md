
<img width="960" height="504" alt="Screenshot 2026-07-17 152046" src="https://github.com/user-attachments/assets/e77d63be-b004-4036-910d-42dbd28ed03f" />
<img width="960" height="504" alt="Screenshot 2026-07-17 150324" src="https://github.com/user-attachments/assets/05ec9bb9-d263-43d5-bf0a-41ddc181fadd" />
<img width="960" height="504" alt="Screenshot 2026-07-17 152222" src="https://github.com/user-attachments/assets/4426e2e9-d4a6-4fc2-930c-992441d4f39a" />
<img width="960" height="540" alt="Screenshot 2026-07-17 152158" src="https://github.com/user-attachments/assets/94a6e393-cd87-45b1-a8dc-870f082f68ea" />

<img width="960" height="504" alt="Screenshot 2026-07-17 150244" src="https://github.com/user-attachments/assets/43f0f49f-e6a2-4357-8a79-fc854a9e0b45" />
# Growfinix Technology Internship - Cybersecurity Tasks

This repository contains the practical tasks completed during my Cybersecurity Internship at *Growfinix Technology*. It demonstrates core concepts of (OSINT), passive reconnaissance, and threat reporting.

---
<img width="960" height="504" alt="Screenshot 2026-07-17 145904" src="https://github.com/user-attachments/assets/b2adaa95-0386-46de-bdd9-ad66e4a8f163" />


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
3. Executed the [Utilities] To DNS Name [Using Name Schema dictionary] transform from the *DNS from Domain* suite


###  Visual Intelligence Discovered
The transform successfully mapped out relationships to major structural endpoints, revealing direct architectural dependencies:
*   admin.owasp.org
*   cloud.owasp.org
*   groups.owasp.org
*   mail.owasp.org
*   www.owasp.org



