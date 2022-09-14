Dean Weiss<br>
14 Sept 2022

# RADIUS Concepts
RADIUS - Remote Authentication Dial In User Service
<br>
In RADIUS the client is responsible for everything in the request.
-Picking an Auth Type
-Authenticating a User
-Insufficient Information


# Computer Network | AAA (Authentication, Authorization and Accounting)

Authentication – 
The process by which it can be identified that the user, which wants to access the network resources, valid or not by asking some credentials such as username and password. Common methods are to put authentication on console port, AUX port, or vty lines. 
As network administrators, we can control how a user is authenticated if someone wants to access the network. Some of these methods include using the local database of that device (router) or sending authentication requests to an external server like the ACS server. To specify the method to be used for authentication, a default or customized authentication method list is used. 

<br>

Authorization – 
It provides capabilities to enforce policies on network resources after the user has gained access to the network resources through authentication. After the authentication is successful, authorization can be used to determine what resources is the user allowed to access and the operations that can be performed. 
For example, if a junior network engineer (who should not access all the resources) wants to access the device then the administrator can create a view that will allow particular commands only to be executed by the user (the commands that are allowed in the method list). The administrator can use the authorization method list to specify how the user is authorized to network resources i.e through a local database or ACS server. 

<br>

Accounting – 
It provides means of monitoring and capturing the events done by the user while accessing the network resources. It even monitors how long the user has access to the network. The administrator can create an accounting method list to specify what should be accounted for and to whom the accounting records should be sent. 

<br>

AAA implementation: AAA can be implemented by using the local database of the device or by using an external ACS server. 

<br>

local database – If we want to use the local running configuration of the router or switch to implement AAA, we should create users first for authentication and provide privilege levels to users for Authorization. 

<br>

ACS server – This is the common method used. An external ACS server is used (can be ACS device or software installed on Vmware) for AAA on which configuration on both router and ACS is required. The configuration includes creating a user, separate customized method list for authentication, Authorization, and Accounting. 
The client or Network Access Server (NAS) sends authentication requests to the ACS server and the server takes the decision to allow the user to access the network resource or not according to the credentials provided by the user. 

<br>

Note – If the ACS server fails to authenticate, the administrator should mention using the local database of the device as a backup, in the method list, to implement AAA.


source: https://wiki.freeradius.org/guide/Concepts
source: https://www.geeksforgeeks.org/computer-network-aaa-authentication-authorization-and-accounting/
