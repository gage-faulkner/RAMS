![alt text](https://s3.wasabisys.com/datamanagement/Downloads/Pictures/Logos/cloud-checked-64.png "RAMS")

RAMS
======
RAMS ─ Remote Asset Management Software ─ is an easy-to-use, lightweight, asset management application that uses a Windows Service to communicate data about Windows PCs to a Google Cloud Firestore NoSQL Database.

Prerequisites
------
|                                                    Logo                                                    |   Publisher   |     Product Name    |  Version |  Size  |                                                            Download                                                           |
|:----------------------------------------------------------------------------------------------------------:|:-------------:|:-------------------:|:--------:|:------:|:-----------------------------------------------------------------------------------------------------------------------------:|
| ![dotNetLogo](https://s3.wasabisys.com/datamanagement/Downloads/Pictures/Logos/dotNet32.png "dotNet Logo") |   Microsoft   |    .NET Framework   |   4.7.2  | 80.1MB | [Click Here](https://s3.wasabisys.com/datamanagement/Downloads/Applications/Microsoft/NDP472-KB4054530-x86-x64-AllOS-ENU.exe) |
| ![ramsLogo](https://s3.wasabisys.com/datamanagement/Downloads/Pictures/Logos/bluelock-32.png "RAMS Logo")  | Gage Faulkner | RAMS Endpoint Agent | 1.91.024 | 60.3MB | [Click Here](https://s3.wasabysys.com/datamanagement/Downloads/Applications/file.txt)                                         |
***

Getting Started
------
Start by downloading the 'RAMS Endpoint Agent' from the table above. Once complete, you're ready to deploy. Please see the tables below for installation procedures along with some examples.

> Please note: The following parameters/args can be entered in any order. The scheme is exactly the same regardless of the switch you're using. (-SWITCH "argument") Be sure there are no spaces after the hyphen and no spaces between the quotation marks.

| Importance | Switch |                              Definition                              | Argument(s) |                               Example                              |
|:----------:|:------:|:--------------------------------------------------------------------:|:-----------:|:------------------------------------------------------------------:|
|  Required  |   -id  |      "Identification" ─ The name of your Firestore DB instance.      |    Custom   |                  `agent.exe -id "exampledb-2370"`                  |
|  Required  |   -d   |  "Department" ─ The 3 letter acronym of the dept the PC belongs to.  |    Custom   |                        `agent.exe -d "AIM"`                        |
|  Required  |   -a   |       "Authentication" ─ URL to your company's .JSON Auth file.      |    Custom   | `agent.exe -a "https://s3.wasabysys.com/data/auth/agentAuth.json"` |
|  Optional  |   -s   | "Silent" ─ Hides the GUI from the end-user. Requires switches above. |  true/false |                        `agent.exe -s "true"`                       |
|  Optional  |   -cd  |   "Change Installation Directory" ─ Changes the installation path.   |    Custom   |               `agent.exe -cid "C:\ProgramData\RAMS\"`              |

##### Here's an example with all switches being used ─
```powershell
agent.exe -id "exampledb-3407" -d "AIM" -a "https://s3.wasabysys.com/data/auth/agentAuth.json" -s "true" -cd "C:\ProgramData\RAMS\"
```
