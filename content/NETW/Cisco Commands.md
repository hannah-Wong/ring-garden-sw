---
title: "Cisco Commands"
draft: false
tags:
  - network
---
 
## Housekeeping
- ### hostname
> hostname *new name*
- ### password/secret
	- #### enable password
	 > enable secret *password*
	- #### console password
	  > line console 0
	   >  password *password*
	   >  login
	- #### encrypt all password
	 > service password-encryption
- ### banner
	- #### motd banner
	 > banner motd # Authorized users only, violators will be yelled at! #
	- #### login banner 
	 > banner login # Authenticate yourself! #
	- #### exec banner 
	 > banner exec # Ensure you update system configuration documentation after making system changes! #
	 > 
- ### interface description
	 > int g0/1
	  > description Connect to R1 interface G0/0
- ### SSH
 > username *username* password *password*
 > ip domain-name *domain name*
 > crypto key generate rsa
 > bits: 1024
 > ip ssh version 2
 > line vty 0 15
 > login local
 > transport input ssh
 - #### ACL
  > ip access-list standard SSHList
  > permit host 11.1.1.1
  > exit
  > line vty 0 15
  > access-class SSHList in
## RADIUS Authentication
[[RADIUS and LDAP Authentication]]]
## Access Control List
[[Access control lists]]
