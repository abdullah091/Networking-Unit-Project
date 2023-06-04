# Networking-Project

1- Create VPC that can have 256 subnet and each subnet can have 256 IP and Name it (Lab-VPC) in Riyadh Region.

2- Create 2 Vswitch in (Lab-VPC)  in Zone A and name first Vswitch (Public-VSwitch-A) and second Vswitch (Private-Vswitch-A).

3- Repeat Task 2 , Create 2 Vswitch in (Lab-VPC) in Zone B and name first Vswitch (Public-VSwitch-B) and second Vswitch (Private-Vswitch-B).

4-Create Security Group that has 2 rule and name it (SecGro) : <br/>
rule 1 :allow| Protocol type (All ICMP IPv4) | Source (0.0.0.0/0). <br/>
rule 2 : allow| Protocol type (Costume TCP) |Port range (SSH 22) | Source (0.0.0.0/0).<br/>

5- Create ECS Instance inside (Private-Vswitch-A) with configuration and name it (Private-ECS): <br/>
Billing Method: Pay-as-you-go . <br/>
Region : Zone A . <br/>
Instance Type : (General Purpose Type g6 ).<br/>
Image : Public Image | ubuntu | 22.04 64bit .<br/>
Clich Next at buttom .<br/>
Network Type : Select Lab-VPC | (Private-Vswitch-A).<br/>
Public IP Address : don't check Assign Public IPv4 Address.<br/>
Security Group : Select SecGro.<br/>
Clich Next at buttom .<br/>
Logon Credentials : select Password | logon Username choose root| in logon password choose your password.<br/>
Clich Next at buttom untill appear Create insance and click on it.<br/>

6- Create ECS Instance inside (Public-Vswitch-B) with configuration and name it (Public-ECS): <br/>
Billing Method: Pay-as-you-go .<br/>
Region : Zone B . <br/>
Instance Type : (General Purpose Type g6 ).<br/>
Image : Public Image | ubuntu | 22.04 64bit <br/>
Clich Next at buttom <br/>
Network Type : Select Lab-VPC | (Public-Vswitch-B).<br/>
Public IP Address :  check box Assign Public IPv4 Address.<br/>
Security Group : Select SecGro.<br/>
Clich Next at buttom .<br/>
Logon Credentials : select Password | logon Username choose root| in logon password choose your password.<br/>
Clich Next at buttom untill appear Create insance and click on it .<br/>

7- Connect to Private-ECS through VNC .

8- After login to Private_ECS :<br/>
     -Enter: (ping alibabacloud.sa) command and take screnshot of output .<br/>
     -Enter: (ping "PRIVATE IP OF Public-ECS") command and take screnshot of output. <br/>
 
 9- Connect to Public-ECS through VNC : <br/>
     -Enter: (ping alibabacloud.sa) command and take screnshot of output. <br/>
     -Enter: (ping "PRIVATE IP OF Private-ECS") command and take screnshot of output. <br/>
     
10- Create internet Nat Gateway to allow private instances to access internet : <br/>
     -Enter: (ping alibabacloud.sa) command and take screnshot of output. <br/>
     



