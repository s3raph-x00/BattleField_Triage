# This Project Is Still In Early Beta #

## BattleField-Triage (BFT) ###
Forensic Triage Toolset

##### Because it is still in early beta, there will be alot of bugs. Please let me know if you run into any issues and I'll try my best to knock them out. #####

### Background: 

    ######################################################################
    ### The name and the methodology stems from a need to be able to   ###
    ### conduct digital media forensics in austere enviornments.       ###
    ### have tried to take various lessons I have learned the hard way ###
    ### and standardize the apporach for organizations needing an open ###
    ### source solution in areas that lack enterprise solutions.       ###
    ### These techniques are not meant to replace such solutions like  ###
    ### F-Response, KAPE, etc.                                         ###
    ######################################################################

### DESCRIPTION:

    ######################################################################
    ### SYNOPSIS:    Collection Starts Either Automated (With Switch), ###
    ###              manually (via CLI), or through the GUI. Triage    ###
    ###              begins with order of volitility once initial info ###
    ###              is collected.                                     ###
    ###              -> 0. Atomospherics.                              ###
    ###              -> 1. Memory.                                     ###
    ###              -> 2. Mandiant Redline Collector (Comprehensive). ###
    ###              -> 3. Forensic Triage Pull (Registry, EVTx, etc). ###
    ###              -> 4. Full Disk Collection.                       ###
    ######################################################################

The core functionality of the tool requires the associated binaries to be in the ./src/ directory. Plan accordingly prior to running. 
- Test software and script prior to using in a live enviorment

### REQUIREMENTS: <br />
Note: Store Binaries (And Their Associated DLLs/Files) In The Following Folder Structure:<br/>
<blockquote>
#   ./BATTLEFIELD_TRIAGE.ps1<br/>
#      ./src/<br/>
#         ./src/ftk/ftkimager.exe<br/>
#         ./src/man/helper.bat<br/>
#         ./src/RamCapture/x64/RamCapture64.exe<br/>
#         ./src/RamCapture/x86/RamCapture86.exe<br/>
#         ./src/Surge/surgecollect.exe<br/>
#         ./src/winpmem.exe<br/>
#         ./src/memoryze/Memoryze.exe<br/>
#         ./src/ShadowSpawn.exe<br/>
</blockquote>

ProTip: _./src/man/_ refers to the Mandiant Redline Collector folder.
    
### Current Development Status 
  1. Windows PowerShell Script
     - [X] Core Functionality <br />
       &#9746; Additional Triage Sources   <br/>
       &#9746; Switches and Parametization<br/>
       &#9746; Testing<br/>
     - [ ] GUI   

##### Legend:
- - [X] - Completed <br />
&#9746; - Partially Completed
- - [ ] - Not Started

##### Known Issues:
  1. Windows PowerShell Script
     - [ ] See Open Issues

### Updating The Core Binaries

When updating various binaries (winpmem for example), ensure the name matches what is currently in the directory and copy over any associated files. 

  **Special Note Regarding Mandiant (FireEye) Redline Collector**: The _helper.bat_ file located in _./src/man/_ has been modified to store forensic artifacts in a relational folder along with the others. Feel free to update (or use different Redline Collection Configurations) but try to match the associated changes in The _helper.bat_ file as seen below:

![fixedinputredline](https://user-images.githubusercontent.com/27127072/129645893-c97f1547-78f7-4ed6-85fa-90b3f709bd9e.png)
   
### Where To Get The Core Binaries: <br />
winpmem: https://github.com/Velocidex/WinPmem <br />
memoryze: [https://www.fireeye.com/services/freeware/memoryze.html](https://fireeye.market/apps/211368) <br />
ramcapture: https://belkasoft.com/ram-capturer <br />
Surge Collect Pro (Not Free): https://www.volexity.com/products-overview/surge/ <br />
FTK Imager (CLI): https://accessdata.com/product-download/ftk-imager-version-4-5 <br />
RedLine Collector: https://www.fireeye.com/services/freeware/redline.html <br />
SpadowSpawn (Still Testing): https://github.com/candera/shadowspawn <br />
