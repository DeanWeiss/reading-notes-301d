Dean Weiss <br>
31 August 2022
<br>
# Active Directory

Active directory is made up of several different directory services:
<ol>
<li> Active Directory Domain Services (AD DS) – the core Active Directory service used to manage users and resources. </li>
<li> Active Directory Lightweight Directory Services (AD LDS) – a low-overhead version of AD DS for directory-enabled applications. </li>
<li> Active Directory Certificate Services (AD CS) – for issuing and managing digital security certificates. </li>
<li> Active Directory Federation Services (AD FS) – for sharing identity and access management information across organizations and enterprises. </li>
<li> Active Directory Rights Management Services (AD RMS) – for information rights management (controlling access permissions to documents, workbooks, presentations, etc.) </li>
<ol>
Fundamental AD features and capabilities include:
<ol>
<li> A schema that defines the classes of objects and attributes contained in the directory. </li>
<li> A global catalog that contains detailed information about every object in the directory. </li>
<li> A query and index mechanism that allows users, administrators, and applications to efficiently find directory information. </li>
<li> A replication service that disseminates directory data across the network. </li>
</ol>
  
Data Structures 
<ul>
<li> A domain is a collection of objects (e.g. users, devices) that share the same Active Directory database. A domain is identified by a DNS name like company.com. </li>
<li> A tree is a collection of one or more domains with a contiguous namespace (they have a common DNS root name like marketing.company.com, engineering.company.com, and sales.company.com). </li>
<li> A forest is a collection of one or more trees that share a common schema, global catalog, and directory configuration—but aren’t part of a contiguous namespace. The forest typically serves as the security boundary for an enterprise network. </li>
</ul>  
  
source: https://www.cyberark.com/what-is/active-directory/
