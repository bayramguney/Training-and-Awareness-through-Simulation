# Training-and-Awareness-through-Simulation

# Training and Awareness through Simulation

## Overview

This lab demonstrates how security awareness training helps organizations defend against phishing and social engineering attacks. The exercise simulates both the attacker and victim perspectives to show how a phishing email can convince a user to execute a malicious file, resulting in a reverse shell connection.

The lab is performed in a controlled environment using Kali Linux and Windows Server, emphasizing cybersecurity awareness rather than offensive exploitation.

---

## Lab Information

- **Lab Type:** Assisted Lab
- **Platform:** Structureality / Skillable
- **Operating Systems:**
  - Kali Linux (KALI)
  - Windows Server 2016 (MS10)
- **Difficulty:** Beginner
- **Focus Areas:**
  - Security Awareness
  - Social Engineering
  - Phishing
  - Reverse Shell Concepts
  - Threat Vectors
  - User Training

---

## CompTIA Security+ Objectives

- **2.2** Explain common threat vectors and attack surfaces.
- **5.6** Given a scenario, implement security awareness practices.

---

# Scenario

As a member of Structureality Inc.'s security team, you explore how phishing attacks succeed by viewing the attack from both the attacker's and victim's perspectives.

The lab demonstrates how a carefully crafted phishing email convinces a user to execute a malicious script. The script downloads additional files and initiates an outbound connection to the attacker's system, illustrating how social engineering can bypass technical defenses when users unknowingly assist the attacker.

The objective is to understand the attack lifecycle so security professionals can better educate users and strengthen organizational defenses.

---

# Skills Demonstrated

- Understanding phishing campaigns
- Recognizing social engineering pretexts
- Identifying attacker tactics
- Understanding reverse shell concepts
- Observing outbound (egress) connections
- Understanding attacker and victim roles
- Security awareness training
- User education strategies
- Network communication basics
- Defensive security analysis

---

# Lab Environment

| Machine | Operating System | Purpose |
|----------|------------------|----------|
| KALI | Kali Linux | Simulated attacker workstation |
| MS10 | Windows Server 2016 | Simulated victim workstation |

---

# Attack Simulation Workflow

```text
Attacker (Kali)
       │
       │ Hosts malicious files
       ▼
Phishing Email
       │
       ▼
Victim opens email
       │
Victim clicks download link
       │
Victim executes script
       │
Script downloads payload
       │
Outbound connection created
       │
       ▼
Attacker receives reverse shell
```

---

# Lab Activities

## 1. Preparing the Attacker Environment

The attacker workstation was configured to host files required for the simulation.

Tasks included:

- Preparing the web server
- Hosting the demonstration files
- Reviewing the simulation scripts
- Starting the Apache web service
- Preparing the reverse shell listener

---

## 2. Creating the Phishing Scenario

The phishing email used a believable support request.

The message claimed:

- equipment upgrades were being performed
- a configuration update was required
- users should download and execute a script
- security warnings could safely be ignored

This demonstrates how attackers use authority, urgency, and trust to persuade users.

---

## 3. Victim Interaction

The simulated victim:

- Opened the phishing link
- Downloaded the batch file
- Executed the downloaded program
- Approved the Windows security prompt

These actions initiated the simulated compromise.

---

## 4. Reverse Shell Demonstration

After execution, the victim machine initiated an outbound connection back to the attacker.

This illustrates an important security concept:

- Many organizations strictly block inbound traffic.
- Outbound traffic is often more permissive.
- Attackers can exploit this by having compromised systems initiate the connection themselves.

---

## 5. Observing the Remote Session

Once connected, the attacker could interact with the victim system through a remote command shell.

The lab demonstrated:

- confirming the target system
- identifying the logged-in user
- observing remote command execution

This portion highlighted the potential impact of a successful phishing attack while remaining within a safe training environment.

---

# Key Security Concepts Learned

## Phishing

A phishing attack attempts to deceive users into revealing information or executing malicious content.

Characteristics include:

- trusted sender names
- urgent requests
- fake support messages
- malicious links
- malicious attachments

---

## Social Engineering

Social engineering targets people instead of technology.

Common techniques include:

- authority
- urgency
- fear
- curiosity
- trust
- helpfulness

---

## Pretexting

A pretext is the believable story attackers use to convince victims to act.

In this lab:

- IT support
- equipment upgrades
- system configuration updates

created a believable scenario.

---

## Reverse Shell

A reverse shell occurs when a compromised computer initiates a connection to an attacker-controlled system.

Advantages for attackers include:

- bypassing many inbound firewall restrictions
- maintaining remote access
- blending into normal outbound traffic

---

## Egress Traffic

Egress traffic refers to outbound network communication leaving an organization's network.

Organizations should monitor outbound traffic because attackers often rely on it for:

- remote control
- malware communication
- data exfiltration
- command and control (C2)

---

# Security Awareness Lessons

Organizations should educate users to:

- Never run unexpected attachments.
- Verify requests before taking action.
- Be cautious of urgent emails.
- Inspect download links carefully.
- Report suspicious messages immediately.
- Never ignore operating system security warnings.
- Contact IT through official channels before installing software.

---

# Defensive Best Practices

Technical controls include:

- Email filtering
- DNS filtering
- Web filtering
- Endpoint Detection and Response (EDR)
- Application allow listing
- Sandboxing attachments
- Multi-Factor Authentication (MFA)
- Security awareness training
- Egress traffic monitoring
- Security Information and Event Management (SIEM)

---

# Real-World Relevance

Phishing remains one of the most common initial access techniques used by cybercriminals and ransomware groups.

Security analysts routinely investigate:

- phishing emails
- malicious attachments
- suspicious downloads
- outbound network connections
- endpoint alerts
- unusual user activity

Understanding both the attacker and victim perspectives improves an analyst's ability to detect and respond to these incidents.

---

# Key Takeaways

- Social engineering targets human behavior rather than technical vulnerabilities.
- A convincing pretext can persuade users to bypass security warnings.
- Reverse shells often leverage outbound connections to evade inbound firewall protections.
- Security awareness training is one of the most effective defenses against phishing attacks.
- Combining user education with layered technical controls significantly reduces organizational risk.

---

# Tools & Technologies

- Kali Linux
- Windows Server 2016
- Apache Web Server
- Netcat (conceptual demonstration)
- Firefox
- Windows Command Prompt

---

# What I Learned

Through this lab, I gained a better understanding of how phishing attacks exploit human trust instead of software vulnerabilities. I observed how a malicious email can lead to unauthorized remote access when a user unknowingly executes a harmful file. I also learned why monitoring outbound network traffic, implementing layered security controls, and providing regular security awareness training are essential for preventing successful social engineering attacks.

---

## Repository Topics

`security-awareness` `phishing` `social-engineering` `reverse-shell` `cybersecurity` `securityplus` `training-lab` `incident-response` `defensive-security` `network-security`
