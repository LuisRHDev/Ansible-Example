Modified production environment ansible configuration files, that will deploy infrastructure as code: 

TOC:
1. Ubuntu Server Joine AD Domain and with additional configuration files, providing remote SSH access through AD Centrally stored/managed KEYS: 
1.1 Ubuntu-Join-Domain.yml  : Prompt's user for credentials and Join's linux workstation to prompted AD Domain.
                                Install's all necessary packages for Samba, NTP and LDAP Kerberose linux client functionality. 
1.2 Ubuntu-Join-Config.yml  : Optional configuration, which allows SSH credentials stored in AD altSecurityIdentities attribute.
                                Users in Domain Admin's group can SSH utilizing their ssh credentials and will have sudoer's access.
                                 No other users will be granted access with this base configuration, this is an admin feature.
                                 service accounts can be created for additional linux system management.


2.  Note: Inventory file will target server group [Linux_systems] and should be provided with -i and linux system password via --ask-pass.
2.2 This configuration, took about 14 hours to complete over Q3 2023 for Linux admin AD System integration.
2.3 Documentation shared on this portal has been edeited and not-tested after removing production/customer environment details and is provided as a technical gallery/portfolio.  
   Execute in your own environment or in production at your own risk (Or just dont without technical expertise into these technologies).  
