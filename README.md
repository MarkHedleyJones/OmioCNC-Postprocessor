# OmioCNC-Postprocessor
If you've got an OmioCNC machine with the [EPL Offline Controller](https://www.omiocnc.com/epl-4f-control-system/) (commonly known as The Orange Box), the postprocessor in this repository will help when generating your `.nc` files.
There are a couple of quirks with the way the controller interprets the `.nc` files which means the standard grbl postprocessor doesn't work properly.
Fortunately, this customised grbl post generation script appears to solve those issues.


## Installation:
Once you have a working installation of Solidworks and HSMWorks (or HSMXpress), add this post processor by following these steps:

* Download the repository as a ZIP file.
* Extract the zip file and copy the file `omio-grbl.cps` into the folder `C:\Program Files\HSMWorks\posts` if you're using HSMWorks or `C:\Program Files\HSMXpress\posts` if you're using HSMXpress.

## Setup HSMWorks/HSMExpress:

Edit the current machine:
![Selecting post file](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/Edit-Machine-edited.PNG)

Select the post setting from the machine configuration page:
![Machine configuration 1](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/MachineConfig1-edited.PNG)

Find the newly copied file in the open file dialog:
![Machine configuration 1](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/MachineConfig2-edited.PNG)

## Usage
Now create your parts and machining operations as usual.
When you go to export the GCode/.nc files (through the Post Process action in HSMWorks) you will see the folowing dialog box:
![Machine configuration 1](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/PostScreen.PNG)

Ensure that the 'omio-grbl.cps' file is selected under Post Configuration field as shown above.

# Notice
I am not affiliated with HSMWorks or OmioCNC.
The post file provided does not come with any warranty and I will not be held liable for any damage that results from your use of this post-processor.
If you have any improvements you wish to share, please do and I'll add them here.
