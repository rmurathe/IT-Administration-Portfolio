Windows Server & Active Directory Lab
Project Overview

This project documents a practical Windows Server and Active Directory laboratory environment created to develop and demonstrate systems administration skills.

The lab simulates a small business IT environment with a Windows Server acting as a Domain Controller and providing core network and directory services to Windows client computers.

Project Objectives

The objectives of the lab were to:

Deploy Windows Server
Configure a static server IP address
Configure DNS
Install and configure Active Directory Domain Services
Create an Active Directory domain
Create Organizational Units
Create users and security groups
Configure Group Policy
Configure DHCP
Join Windows client computers to the domain
Configure file and folder sharing
Troubleshoot domain connectivity
Develop practical Windows Server administration skills
Lab Environment
Server

Operating System: Windows Server 2022 Standard

Primary roles:

Active Directory Domain Services
DNS Server
DHCP Server
File Services
Client

Operating System: Windows client

The client computer was configured to communicate with the Windows Server and participate in the Active Directory domain.

Network

The laboratory uses a private IPv4 network.

Actual internal IP addresses and company network details are intentionally omitted from this public repository.

Windows Server Configuration

The server was configured with a static IPv4 address to provide a predictable address for infrastructure services.

Configuration included:

Static IPv4 addressing
Subnet configuration
Default gateway
Preferred DNS configuration
Hostname configuration

The server was then prepared for installation of the required Windows Server roles.

Active Directory Domain Services

Active Directory Domain Services was installed and configured to provide centralized identity and computer management.

The configuration included:

Active Directory Domain Services installation
Domain Controller promotion
Domain creation
Active Directory Users and Computers
Organizational Units
User accounts
Security groups
Computer accounts
Organizational Units

Organizational Units were used to provide logical organization of users and computers.

Example structure:

Company
│
├── Users
│   ├── Administration
│   ├── Finance
│   ├── Sales
│   └── IT
│
├── Computers
│   ├── Workstations
│   └── Laptops
│
└── Groups

The structure can be expanded according to the organization's requirements.

DNS

DNS was configured as part of the Active Directory environment.

DNS is essential for Active Directory because domain clients use DNS to locate domain services and communicate with the Domain Controller.

Testing included:

DNS resolution
Server name resolution
Client-to-server connectivity
Domain Controller discovery
DHCP

DHCP was configured to provide automatic network configuration to client computers.

The DHCP configuration included:

IPv4 scope
Address range
Subnet configuration
Default gateway
DNS server
Address reservations where required

This reduced the need to manually configure network settings on client computers.

Users and Security Groups

Test user accounts were created within appropriate Organizational Units.

Security groups were used to simplify permissions management.

Example groups included:

IT-Administrators
Finance-Users
Sales-Users
Standard-Users

Group-based administration provides a scalable method of managing access to organizational resources.

Group Policy

Group Policy was explored to centrally manage Windows client settings.

Examples of policies that can be applied include:

Password policies
Account lockout policies
Desktop configuration
Security settings
Windows configuration
Software restrictions
User environment settings

The lab demonstrates how Group Policy can be used to manage multiple computers centrally.

Client Domain Join

A Windows client computer was configured to join the Active Directory domain.

The process included:

Configuring the client DNS settings
Testing network connectivity
Confirming DNS resolution
Joining the domain
Restarting the client
Signing in with a domain account
Confirming the computer account in Active Directory
File Sharing

Windows file sharing was configured to demonstrate centralized access to network resources.

The lab explored:

Shared folders
NTFS permissions
Share permissions
User access
Group-based permissions

The principle of least privilege was considered when assigning access.

Troubleshooting

Several common Windows Server and Active Directory troubleshooting scenarios were explored.

Examples include:

Domain Controller Connectivity

When a client cannot contact the Domain Controller, troubleshooting can include checking:

Network connectivity
IP configuration
DNS settings
Server availability
Active Directory services
Firewall configuration
DNS Problems

DNS troubleshooting included checking:

ipconfig /all
nslookup
ping

Correct DNS configuration is particularly important in an Active Directory environment.

Domain Join Problems

Domain-join troubleshooting involved checking:

Client DNS configuration
Domain name resolution
Network connectivity
Domain Controller availability
Credentials
Windows firewall settings
Security Considerations

The public GitHub documentation intentionally excludes:

Real passwords
Internal credentials
Private company information
Actual internal IP addresses
Sensitive network configuration
Personal user information

All examples shown in this repository are intended for educational and portfolio purposes.

Skills Demonstrated

This project demonstrates practical knowledge of:

Windows Server administration
Active Directory
Active Directory Domain Services
DNS
DHCP
Group Policy
User administration
Security groups
Organizational Units
Domain joining
File sharing
NTFS permissions
Network troubleshooting
Windows troubleshooting
IT documentation
Lessons Learned

The project reinforced the importance of DNS, correct IP configuration, and network connectivity when deploying Active Directory.

It also demonstrated how centralized identity management can simplify administration of users, computers, permissions, and security policies.

Future Improvements

Future improvements to the laboratory environment could include:

Windows Server redundancy
Additional Domain Controller
Advanced Group Policy
File server quotas
Windows deployment services
PowerShell administration
Microsoft Entra ID integration
Endpoint management
Centralized logging
Security monitoring
Backup and disaster recovery
Author

Reginald Murathe

IT Support | Systems Administration | Network Administration | IT Infrastructure

Kenya
