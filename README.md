# Enumeration
Enumeration Techniques

# Explore Google hacking and enumeration 

# AIM:

To use Google for gathering information and perform enumeration of targets

## STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode

### Step 2:

Investigate on the various Google hacking keywords and enumeration tools as follows:


### Step 3:
Open terminal and try execute some kali linux commands

## Pen Test Tools Categories:  

Following Categories of pen test tools are identified:
Information Gathering.

Google Hacking:

Google hacking, also known as Google dorking, is a technique that involves using advanced operators to perform targeted searches on Google. These operators can be used to search for specific types of information, such as sensitive data that may have been inadvertently exposed on the web. Here are some advanced operators that can be used for Google hacking:

site: This operator allows you to search for pages that are within a specific website or domain. For example, "site:example.com" would search for pages that are on the example.com domain.
Following searches for all the sites that is in the domain yahoo.com

<img width="1895" height="977" alt="632164562-8e429534-7249-4d86-b36a-4138e2ef3864" src="https://github.com/user-attachments/assets/e8605938-3fec-40ab-8412-9d138f039549" />


filetype: This operator allows you to search for files of a specific type. For example, "filetype:pdf" would search for all PDF files.
Following searches for pdf file in the domain yahoo.com


<img width="1890" height="982" alt="632164829-693681ae-52c3-4013-98bb-acb0cd2492ee" src="https://github.com/user-attachments/assets/8d49644b-6766-4525-9bd6-3de473860b80" />





intext: This operator allows you to search for pages that contain specific text within the body of the page. For example, "intext:password" would search for pages that contain the word "password" within the body of the page.


<img width="1893" height="986" alt="632165928-6b7fa9c5-6235-451e-b6bf-3c4a4243766c" src="https://github.com/user-attachments/assets/0e40a8ef-eea9-43fa-94a6-57632db01ea1" />


inurl: This operator allows you to search for pages that contain specific text within the URL. For example, "inurl:admin" would search for pages that contain the word "admin" within the URL.


<img width="1901" height="991" alt="632166584-750f2bcc-e35d-423c-8318-6f46f5a84266" src="https://github.com/user-attachments/assets/ffd1e0f3-0276-483b-bac5-bddd8e5c165f" />


intitle: This operator allows you to search for pages that contain specific text within the title tag. For example, "intitle:index of" would search for pages that contain "index of" within the title tag.


<img width="1897" height="987" alt="632167057-d8bf1cf5-3b0f-4179-8e04-d8e88cb83a28" src="https://github.com/user-attachments/assets/a5d8f4da-91df-4b3e-902b-5f8185163a2c" />


link: This operator allows you to search for pages that link to a specific URL. For example, "link:example.com" would search for pages that link to the example.com domain.


<img width="1896" height="995" alt="632167643-596c8bdc-6e4a-4873-90e9-182a8319eaf5" src="https://github.com/user-attachments/assets/c2b74f93-7da8-4e04-801a-d459195a6a3b" />


cache: This operator allows you to view the cached version of a page. For example, "cache:example.com" would show the cached version of the example.com website.


<img width="1902" height="987" alt="632352274-7d66bf81-6176-4849-93b9-246fd85b75de" src="https://github.com/user-attachments/assets/a6bcf055-0d54-47fc-a0c3-e7021c9034ad" />


 
#DNS Enumeration


## DNS Recon
provides the ability to perform:
Check all NS records for zone transfers
Enumerate general DNS records for a given domain (MX, SOA, NS, A, AAAA, SPF , TXT)
Perform common SRV Record Enumeration
Top level domain expansion
## OUTPUT:

<img width="712" height="835" alt="632175709-10aaa45a-d2c9-476c-8029-6eab197d9344" src="https://github.com/user-attachments/assets/d39d64bb-e7f8-4051-9fbd-b86d381ccc93" />



<img width="628" height="606" alt="632175809-36f2cd7d-a2a5-43c9-8b98-cc4e82f99ac7" src="https://github.com/user-attachments/assets/34961a67-f171-4235-9a8a-26aeb8554963" />








##dnsenum
Dnsenum is a multithreaded perl script to enumerate DNS information of a domain and to discover non-contiguous ip blocks. The main purpose of Dnsenum is to gather as much information as possible about a domain. The program currently performs the following operations:

Get the host’s addresses (A record).
Get the namservers (threaded).
Get the MX record (threaded).
Perform axfr queries on nameservers and get BIND versions(threaded).
Get extra names and subdomains via google scraping (google query = “allinurl: -www site:domain”).
Brute force subdomains from file, can also perform recursion on subdomain that have NS records (all threaded).
Calculate C class domain network ranges and perform whois queries on them (threaded).
Perform reverse lookups on netranges (C class or/and whois netranges) (threaded).
Write to domain_ips.txt file ip-blocks.
This program is useful for pentesters, ethical hackers and forensics experts. It also can be used for security tests.


## smtp-user-enum

Username guessing tool primarily for use against the default Solaris SMTP service. Can use either EXPN, VRFY or RCPT TO.


In metasploit list all the usernames using head /etc/passwd or cat /etc/passwd:

select any username in the first column of the above file and check the same
## Output

<img width="637" height="363" alt="632176159-ba6ef329-0ebf-4be5-94a5-07e8678a5755" src="https://github.com/user-attachments/assets/60945736-fe91-495c-9ab8-81009a567ab2" />



## Telnet for smtp enumeration

Telnet allows to connect to remote host based on the port no. For smtp port no is 25
telnet <host address> 25 to connect
and issue appropriate commands
  
 ## Output
   
  <img width="375" height="337" alt="632358088-67ec7483-d8f6-4648-a35b-f85822004ec4" src="https://github.com/user-attachments/assets/5bba13de-7fd8-4e7e-9892-a6b07dc824ac" />


## nmap –script smtp-enum-users.nse <hostname>

The smtp-enum-users.nse script attempts to enumerate the users on a SMTP server by issuing the VRFY, EXPN or RCPT TO commands. The goal of this script is to discover all the user accounts in the remote system.


## OUTPUT:

<img width="620" height="180" alt="632365741-957e7143-9141-456d-958e-02d1a60f60b3" src="https://github.com/user-attachments/assets/8ab57c32-7f03-40cc-a8e3-c90cb6674e81" />


## RESULT:
The Google hacking keywords and enumeration tools were identified and executed successfully

