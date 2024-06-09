## Azure Virtual Machine
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/VMSpecifications.png?raw=true)

Following resources have been created under the group for VM


| Resource   | Description                                          |
|------------|------------------------------------------------------|
| ovm        | Virtual Machine                                      |
| ovm-ip     | Public IP address                                    |
| ovm-nsg    | Firewall to restrict incoming/outgoing traffic       |
| ovm616_z1  | Virtual network card for data transmission           |
| disk       | Assigned virtual disk                                |
| ovm-vnet   | Hosting virtual machine                              |

<details>
   <summary markdown="span" style="cursor:pointer;"><h2 style="margin:0;">Setup IIS on VM</h2></summary>
  


1- Press win + R

2- open "Server Manager"

3- "Add roles and features"

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/1.png?raw=true)

4- Check Web Server IIS

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/2.png?raw=true)

5- Don't change anything until necessary and Install

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/3.png?raw=true)

</details>
<details>
   <summary markdown="span" style="cursor:pointer;"><h2 style="margin:0;">Configure Network for Website Hosting</h2></summary>


On VM, if you will go to the http://localhost it will be working fine
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/IISLocal.png?raw=true)

Go to the Network settings on Azure VM Portal 

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/Networking.png?raw=true)

Add Inbound Security Rule

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/networking2.png?raw=true)

This ensure the connectivity on port 80

</details>


