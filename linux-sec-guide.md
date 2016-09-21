# Linux Desktop Security Guide: A Checklist of Sorts

## Overview

1. Introduction
2. Basic Security Concepts
3. User Accounts
4. Authentication
5. Access Control
6. Configuration Management
7. Encryption
8. Integrity
9. Kernel Hardening
10. Network Security
11. Auditing
12. References

## Introduction
### Disclaimer
### Who is this for?
### Why does this matter?
### Contributing

## Basic Security Concepts
### Confidentiality
#### Encryption
When implemented correctly, encryption is the most secure method of providing confidentiality. In it's most basic form, an encryption algorithm scrambles the data passed to it in such a way that the output is unreadable and reveals as little as possible about the original input data. There are many ciphers available but the wisest choice is to go with ciphers that have been around the longest and have withstood the test of time. A full technical description of cryptography and all that goes along with it is too big and complex of a subject to cover here. Cryptography is a very fascinating, though dense, subject. I would definitely recommend learning the concepts behind cryptographic algorithms to better understand how to properly choose the best cryptosystem for your needs.
#### Access Controls
Access control is provided through identification, authentication, and finally, authorization. Once a user has claimed an identity and proven that identity using some form of authentication, the system can then grant or restrict access to resources using an authorization method, such as permissions.

### Integrity
Verifying the integrity of data provides assurance that it has not been modified, tampered with, or corrupted in any way, whether through unintentional error or intentional unauthorized access. There are some very easy ways of verifying the integrity of data. The most common of these is hashing.
#### Hashing
The most common and secure method of verifying the integrity of a piece of data is through the use of a hashing algorithm. The data is fed to the algorithm, which then produces a unique string. As long as the data fed to the algorithm has not changed in any way, the hashing algorithm will always produce the same hash.

Hashing is also used to verify that we have a valid copy of a piece of data, such as a binary, that has not been modified or corrupted in transit. It is common for software packages on the internet to come with hashes so users can verify the integrity of the package.
#### Digital Signatures
Digital signatures are a way of verifying the owner or source of data. They also provide authentication and non-repudiation. Be aware of this detail as non-repudiation eliminates plausible deniability. If you value privacy and want to remain anonymous, remember this when using digital signatures and some other forms of authentication.

### Least Privilege Access
The concept of least privilege is a simple one: only provide the minimum amount of privilege a user/process needs in order to perform necessary tasks. For example, there is no reason for a normal user to be able to see what processes other users are running, or to read sensitive system configuration files in /etc. By restricting users and processes to only the data they need to function, it becomes much harder for rogue users/processes to cause harm or gather sensitive information.

### Risk
#### Risk Management
#### Threat Modeling

## User Accounts
### Account Management Concepts
### Hardening Root
### Account Lockout

## Authentication
### Factors of Authentication
### Passwords
#### Creating Strong Passwords
#### Password Length
#### Keyspaces
#### Password History
### Authentication Services

## Access Control
### Access Control Overview
### Permissions
### Role based access management (RBAC)

## Configuration Management

## Encryption
### Overview
### Types of Cryptographic Algorithms
### Protocols, Modes, and Parameters
### Disk Encryption
#### Tools
#### Parameters
#### Disk Preparation
#### Example: An FDE Walkthrough
#### Caveats and Limitations
#### Attacks Against FDE
#### Mitigations
### Filesystem Encryption
#### Tools
#### Caveats and limitations
### File encryption
#### Tools
#### Caveats and limitat

## Integrity

## Kernel Hardening
### Kernel Hardening Concepts
### Exploit Mitigation Techniques
#### Address Space Layout Randomization (ASLR)
#### Stack Protections
#### Memory Segmentation
### Tools

## Network Security
### Networking Overview
### Firewalls
### Intrusion Detection
### Common Services
### Anonymization

## Auditing
### Vulnerability Assessment
### Penetration Testing
### Log Auditing
### Rootkit Checks
### Indicators of Compromise

## References
