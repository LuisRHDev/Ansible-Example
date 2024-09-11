**Main: ** Modified production environment ansible configuration files, that will deploy infrastructure as code: 

1- **Ubuntu Server Join AD Domain and AD user remote access** provides remote SSH access through AD Centrally stored/managed KEYS: 

1.a. **Ubuntu-Join-Domain.yml**  : Prompt's user for credentials and Join's linux workstation to prompted AD Domain.
                                Install's all necessary packages for Samba, NTP and LDAP Kerberose linux client functionality. 

1.b. **Ubuntu-Join-Config.yml**  : Optional configuration, which allows SSH credentials stored in AD altSecurityIdentities attribute.
                                Users in Domain Admin's group can SSH utilizing their ssh credentials and will have sudoer's access.
                                 No other users will be granted access with this base configuration, this is an admin feature.
                                 service accounts can be created for additional linux system management.


2- Note: Inventory file will target server group [Linux_systems] and should be provided with -i and linux system password via --ask-pass.
2.a. This configuration, took about 14 hours to complete over Q3 2023 for Linux admin AD System integration.
2.b. This documentation is being published for technical review and as a professional body of work. Configuration has not been tested after editing to removing production/customer environment details.

-- **Execute in your own environment or in production at your own risk (Or just dont without technical expertise into these technologies).  **
