# Active-Directory-Lab
Created an Active Directory lab to practice interacting and managing users in comparison to help desk roles. Also used for practice with remote desktoping to devices on the domain for troubleshooting
The contents listed below will be the configuration of my Domain Controller VM and the Windows server 
My first step was downloading the Windows Server 2022 iso file and putting this OS into VirtualBox
In VB Network settings, make sure the connection is set to "Host adapter only" to ensure that any devices added to the network can only communicate with the host Computer for security purposes.
Made sure to change the name of my Server to a specific name value that shows its function and Purpose<img width="1024" height="768" alt="github 1" src="https://github.com/user-attachments/assets/f2ddbc21-3879-4469-8ac2-3dbfacae4ad6" />
Configured my Domain Controller VM through the Control Panel and made sure the DNS was the same IP as the VM so that any domain services or queries can recognize this domain controller as the DNS to resolve. Also, to maintain the security of the lab enviroment <img width="1024" height="768" alt="github 2" src="https://github.com/user-attachments/assets/66cc183b-8291-4490-a2ba-4af5b90d2e6c" />
Ran PowerShell commands Ipconfig/all to confirm proper configuration was implemented, and ran "Ping" (yourIp-address) to confirm connectivity of the Domain Controller <img width="1024" height="768" alt="Github 3" src="https://github.com/user-attachments/assets/170144ba-5227-4a2c-bff5-7ec7b05ba19f" />
To make my server actually my Domain controller I went through Windows server 2022 clicked "add new forest" labeled the domain name, afterwards i went to the Tools > DNS> Forwaders and added my VM Ip address to be the forwarder so that any resolutions that devices connected to my network will be sent to my Domain Controller IP <img width="1024" height="768" alt="VirtualBox_Domaincontroller_25_03_2026_12_16_41" src="https://github.com/user-attachments/assets/36943342-364d-4657-afb7-2de66a222993" />
Went to Tools > Active Directory> labs. local and created organizational units to group my users in, so that group policies/permissions that are made affect all users in specific groups <img width="1024" height="768" alt="VirtualBox_Domaincontroller_25_03_2026_12_25_07" src="https://github.com/user-attachments/assets/659d91c1-9428-48c7-b152-03c3034b31f3" />
Set up password policies for users by editing the domain Policies so users must implement longer passwords,<img width="1024" height="768" alt="VirtualBox_Domaincontroller_25_03_2026_12_30_57" src="https://github.com/user-attachments/assets/1acd6c6e-dc8c-4a2d-880f-d8eeb043f85e" />     This is the Password policy in action <img width="1024" height="768" alt="github 6" src="https://github.com/user-attachments/assets/cae14fa4-c620-4b43-9f85-91f0320dcdc8" />
Once done, I went to the PowerShell command line to fully confirm that my users and groups were configured correctly by importing my Active Directory and inputting the command
s to ensure completion
Importing Active Directory
<img width="1024" height="768" alt="Github 7" src="https://github.com/user-attachments/assets/680cfe4c-0b0c-4963-9e0b-50e873eaedfc" /> 
Verifying Users and Groups are properly created
<img width="1024" height="768" alt="Github 8" src="https://github.com/user-attachments/assets/34a19761-ffc2-474e-bbd1-e3b55ae87b45" />
Displays members of Groups created
<img width="1024" height="768" alt="Github 9" src="https://github.com/user-attachments/assets/45fa608f-3986-4431-a8ca-fb7d1efa4568" />


