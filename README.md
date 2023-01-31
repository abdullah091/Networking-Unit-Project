# Networking-Project

1- Create VPC that can have 256 subnet and each subnet can have 256 IP and Name it (Lab-VPC) in Riyadh Region.

2- Create 2 Vswitch in (Lab-VPC)  in Zone A and name first Vswitch (Public-VSwitch-A) and second Vswitch (Private-Vswitch-A).

3- Repeat Task 2 , Create 2 Vswitch in (Lab-VPC) in Zone B and name first Vswitch (Public-VSwitch-B) and second Vswitch (Private-Vswitch-B).

4-Create Security Group that has 2 rule and name it (SecGro) : 
rule 1 :allow| Protocol type (All ICMP IPv4) | Source (0.0.0.0/0). 
rule 2 : allow| Protocol type (Costume TCP) |Port range (SSH 22) | Source (0.0.0.0/0) .

5- Create ECS Instance inside (Private-Vswitch-A) with configuration and name it (Private-ECS): <br/>
Billing Method: Pay-as-you-go .
Region : Zone A . 
Instance Type : (General Purpose Type g6 ).
Image : Public Image | ubuntu | 22.04 64bit .
Clich Next at buttom .
Network Type : Select Lab-VPC | (Private-Vswitch-A).
Public IP Address : don't check Assign Public IPv4 Address.
Security Group : Select SecGro.
Clich Next at buttom .
Logon Credentials : select Password | logon Username choose root| in logon password choose your password.
Clich Next at buttom untill appear Create insance and click on it .

6- Create ECS Instance inside (Public-Vswitch-B) with configuration and name it (Public-ECS): 
Billing Method: Pay-as-you-go .<br/>
Region : Zone B . <br/>
Instance Type : (General Purpose Type g6 ).
Image : Public Image | ubuntu | 22.04 64bit <br/>
Clich Next at buttom 
Network Type : Select Lab-VPC | (Public-Vswitch-B).
Public IP Address :  check box Assign Public IPv4 Address.
Security Group : Select SecGro.
Clich Next at buttom .
Logon Credentials : select Password | logon Username choose root| in logon password choose your password.
Clich Next at buttom untill appear Create insance and click on it .

7- Connect to Private-ECS through VNC .

8- After login to Private_ECS :
     1-Enter: (ping google.com) command and take screnshot of output .
     2-Enter: (ping "PRIVATE IP OF Public-ECS") command and take screnshot of output. 
 
 9- Connect to Public-ECS through VNC :
     1-Enter: (ping google.com) command and take screnshot of output .
     2-Enter: (ping "PRIVATE IP OF Private-ECS") command and take screnshot of output. 
     




