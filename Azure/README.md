
# Azure Services

A brief description of how to configure and deploy dot NET project on VM Windows, Linux


<details>
   <summary markdown="span" style="cursor:pointer;"><h2 style="margin:0;">Virtual Machine</h2></summary>
  
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
   <summary markdown="span" style="cursor:pointer;"><h2 style="margin:0;">Windows VM</h2></summary>

Desciption of the configuration of Window VM, Netork Settings and deployement of a dot NET Project

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


### Configure Network for Website Hosting

On VM, if you will go to the http://localhost it will be working fine
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/IISLocal.png?raw=true)

Go to the Network settings on Azure VM Portal 

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/Networking.png?raw=true)

Add Inbound Security Rule

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/networking2.png?raw=true)

This ensure the connectivity on port 80

</details>

<details>
   <summary markdown="span" style="cursor:pointer;"><h2 style="margin:0;">Deloying a Project on VM</h2></summary>


### Configure Network for Website Hosting

When you will start publishing through Azure in VS Studio, this error might happen
![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/error.png?raw=true)

Go to the Overview -> Public IP -> Configuration
make IP Static and assgn some DNS name as follows and save

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/DNS.png?raw=true)

Add Inbound Security Rule

![App Screenshot](https://github.com/talha469/Documentation/blob/main/Common/Media/networking2.png?raw=true)

This ensure the connectivity on port 80

</details>

</details>

</details>

## Badges

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://choosealicense.com/licenses/mit/)

## Feedback

If you have any feedback, please reach out to me at talhaarshad469@gmail.com

