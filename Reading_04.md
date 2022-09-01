Dean Weiss<br>
1 Sept 2022
<br>
# What is a Group Policy
It is a feature of Windows that facilitates a wide variety of advanced settings that network admins can use to control the working environment of users and computers accounts in Active Directory. It essentially provides a centralized place for administrators to manage and configure operating systems, applications and users’ settings.

### Group Policy Object (GPO)?
A Group Policy Object (GPO) is a group of settings that are created using the Microsoft Management Console (MMC) Group Policy Editor. GPOs can be associated with a single or numerous Active Directory containers, including sites, domains, or organizational units (OUs). The MMC allows users to create GPOs that define registry-based policies, security options, software installation and much more.
<br>
Active Directory applies GPOs in the same, logical order; local policies, site policies, domain policies and OU policies.

### How are GPO proceessed?
The order that GPOs are processed is known as LSDOU, which stands for local, site, domain, organizational unit. The local computer policy is the first to be processed, followed by the site level to domain AD policies, then finally into organization units. If there happen to be conflicting policies in LSDOU, the last applied policies wins out.

### Benefits of Group Policy for Data Security?
It allows the system administrator to monitor and establish rules that effect, Passwords Policy, Systems Management and Health Checking.

### Drawbacks?
Not a very friendly user system. Powershell can help mitigate this. They are undertaken randomly between 90-120 min or set to update ever 0 Minutes to 45 days, if set to 0 it will try and update every 7 seconds, which can choke the network with traffic. They are also not immune to Cyberattacks. 

## What would I like to know more about?
What other tools work well along with GPO to help Network Admins monitor and control their network? Is there anything that is user-friendly and more intuitive?

Sources: [Lepide](https://www.lepide.com/blog/what-is-group-policy-gpo-and-what-role-does-it-play-in-data-security/)
