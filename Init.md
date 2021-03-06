## Reference to Init_v2019r1
### Scripts Language

All the __Reference to Init_v2019r1__ box is written in Dynamic Java.

__Reference to Init_v2019r1__ Workflow part contains three boxes :

- *__Get JobID__ box written in Java language*
- *__Initialization__ box written in Java language*
- *__Copy Scripts & Manage Rights__ written in Bash (Shell UNIX language).*

### What boxes do ?

This Workflow sub-part allows the initialization of the different paths and the construction of the paths for each execution (for each frequency of each configuration through the *JobID*).

This sub-part is separated into three boxes which are linked together.

__Get JobID :__

*The script __Get JobID__ allows you to determine on which directory to work by calling on the JobID which will allow us to create the different paths and directories later.*

__Initialization :__

*This script makes it possible, to obtain the name of study, to obtain the name of the various processes, the construction of the Numacous Folder path according to the JobID.*

__Copy Scripts & Manage Rights :__

*__Copy Scripts & Manage Rights__ script allows the folders copy and rights managing*


__Reference to Init_v2019r1__ subpart is preceded by the __Set ANANAX environment and resources PATH__ box, which consist in variable environment sourcing (necessary for the execution of the various workflow scripts) and followed by the __Create Folders__ box which consist in the repository creation (contained in the *namesOfFolder* agregate).

![Initialization components](https://user-images.githubusercontent.com/45098441/72733867-08afde80-3b99-11ea-88fb-0736ee0ea2e3.jpeg)

![Details](https://user-images.githubusercontent.com/45098441/72733862-02216700-3b99-11ea-90d0-fba2f892a949.jpeg)

----------------------------


### Which files to import ?

To execute these scripts correctly, we need to import Python libraries.
The table below lists all the imports to be made for each box :

__For the Get JobID box :__

| Import name | Import location |
| :------: | :------: |
| XMLAnanax2dCanonicalIntake | `/python/api/ductnoise/fannoise/ananax/ananax2d_canonical_intake` |
| Logger | `/python/workflows/common` |

__For the Initialization box :__

| Import name | Import location |
| :------: | :------: |
| XMLAnanax2dCanonicalIntake | `/python/api/ductnoise/fannoise/ananax/ananax2d_canonical_intake` |
| Logger | `/python/workflows/common` |

__For Copy Scripts & Manage Rights box :__

| Import name | Import location |
| :------: | :------: |
| XMLAnanax2dCanonicalIntake | `/python/api/ductnoise/fannoise/ananax/ananax2d_canonical_intake` |
| Logger | `/python/workflows/common` |

### What about variables ?

The table below lists all the variables to be created in Isight and their role :

__Inputs variables to be given to Isight or received from previous boxes :__ 

__Init general subpart :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| loggerNameOfMetaComponent | Logger name of meta component | STRING | X | - |
| loggerVerbosity | Logger verbosity | STRING | X | - |
| nameOfFiperscratchInputXML | Name of Fiper scratch input XML | STRING | X | - |
| nameOfFiperscratchMonitoring | Name of Fiper scratch monitoring | STRING | X | - |
| nameOfLogsFolder | Name of logs directory | STRING | X | - |
| nameOfMonitoringTemplate | Name of monitoring template | STRING | X | - |
| nameOfScriptsFolder | Name of scripts directory | STRING | X | - |
| numericalStudyAOPYear | Numerical study AOP year | STRING | X | - |
| numericalStudyName | Name of the numerical study | STRING | X | - |
| numericalStudyUsecase | Use case of the numerical study | STRING | X | - |
| pathOfApplicationRootFolder | Path of the application root folder | STRING | X | - |
| pathOfJavaSrcFolder | Path of the java source directory | STRING | X | - |
| pathOfResourcesFolder | Path of resources directory | STRING | X | - |
| processCommand | Process command | STRING | X | - |
| processName | Name of the process | STRING | X | - |
| processNameOfApplication | Process name of the Application | STRING | X | - |
| processVersion | Process version | STRING | X | - |
| subwfInitPathOfRootFolder | Sub workflow path of root directory | STRING | X | - |
| subwfInitVersion | Sub workflow init version | STRING | X | - |

__Initialization box :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| nameOfComponent | Input XML which contain all data | FILE | X | - |
| nameOfMetaComponent | Python source folder wich contain all librairies | STRING | X | - |
| verbosity | Python source folder wich contain all librairies | STRING | X | - |
| nameOfFiperscratchInputXML| Python source folder wich contain all librairies | STRING | X | - |
| nameOfFiperscratchMonitoring | Python source folder wich contain all librairies | STRING | X | - |
| nameOfLogsFolder| Python source folder wich contain all librairies | STRING | X | - |
| nameOfScriptsFolder | Python source folder wich contain all librairies | STRING | X | - |
| AOPYear | Python source folder wich contain all librairies | STRING | X | - |
| name | Python source folder wich contain all librairies | STRING | X | - |
| usecase | Python source folder wich contain all librairies | STRING | X | - |
| pathOfJobFolder | Python source folder wich contain all librairies | STRING | X | - |
| pathOfNumacousRootFolder | Python source folder wich contain all librairies | STRING | X | - |
| command | Python source folder wich contain all librairies | STRING | X | - |
| name | Python source folder wich contain all librairies | STRING | X | - |
| nameOfMonitoringTemplate | Python source folder wich contain all librairies | STRING | X | - |
| pathOfResourcesFolder | Python source folder wich contain all librairies | STRING | X | - |
| processNameOfApplication | Python source folder wich contain all librairies | STRING | X | - |
| version | Python source folder wich contain all librairies | STRING | X | - |
| subwfInitPathOfRootFolder | Python source folder wich contain all librairies | STRING | X | - |
| subwfInitVersion | Python source folder wich contain all librairies | STRING | X | - |

__Copy Scripts & Manage Rights box :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| nameOfScriptsFolder | Python source folder wich contain all librairies | STRING | X | - |
| pathOfApplicationRootFolder | Python source folder wich contain all librairies | STRING | X | - |
| pathOfJavaSrcFolder | Python source folder wich contain all librairies | STRING | X | - |
| pathOfJobFolder | Python source folder wich contain all librairies | STRING | X | - |
| processNameOfApplication | Python source folder wich contain all librairies | STRING | X | - |


__Outputs variables to send to following boxes :__

__Init general subpart :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| pathOfJavaSrcFolder | Input XML which contain all data | FILE | - | X |
| pathOfNumacousFolder | Python source folder wich contain all librairies | STRING | - | X |
| userCompany | Python source folder wich contain all librairies | STRING | - | X |
| userEmail | Python source folder wich contain all librairies | STRING | - | X |

__Get JobID box :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| pathOfJobFolder | Job Folder path (for each configuration) | STRING | - | X |
| pathOfNumacousRootFolder | Numacous Root Folder | STRING | - | X |

__Initialization box :__

| Variable Name | Variable description | Type | Input | Output |
| ------ | :------------: | :------: | :------: |  :------: |
| isNis | True if input is Nis Airbus type | BOOLEAN | - | X |
| pathOfNumacousFolder | Numacous Root Folder | STRING | - | X |
| company | User Company | STRING | - | X |
| email | User Email adress to send workflow status | STRING | - | X |
