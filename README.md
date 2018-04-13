# OmioCNC-Postprocessor
If you've got an OmioCNC machine with the [EPL Offline Controller](https://www.omiocnc.com/epl-4f-control-system/) (commonly known as The Orange Box), the postprocessor in this repository will help when generating your `.nc` files.
There are a couple of quirks with the way the controller interprets the `.nc` files which means the standard grbl postprocessor doesn't work quite right.
Fortunately, this customised grbl post generation script will have your CNC running with popular CAM packages such as Fusion360 and HSMWorks/HSMExpress.


## Installation into Fusion 360:

### Download and extract the post-processor:
* Download the repository as a ZIP file.
* Extract the zip file and copy the file `omio-grbl.cps` into the folder `C:/Users/[Username]/AppData/Local/Autodesk/webdeploy/production/[Unique Installation ID]/Applications/CAM360/Data/Posts/`. For example on my system this looks like:  `C:/Users/Mark/AppData/Local/Autodesk/webdeploy/production/8556a3e1d81f6c5f0bca3f1440fbfa311d80a809/Applications/CAM360/Data/Posts/`

### Configure Fusion 360:

Create a basic part (or open an existing one) so we can access the Post-Processor dialog box.
![Create basic part](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/Fusion360-BasicPart.PNG)

Open the CAM Workspace (top left dropdown)
![Open cam workspace](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/Fusion360-OpenCAMWorkspace.PNG)

Add a basic cam operation (ignore this step if you've already got an operation from an existing part).
![Basic cam operation](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/Fusion360-BasicCAMOperation.PNG)

Select the OmioCNC post-processor (omio-grbl) from the available post-processors.
![Select omio-grbl](https://raw.githubusercontent.com/MarkHedleyJones/OmioCNC-Postprocessor/master/images/Fusion360-SelectPostConfiguration.PNG)

## Installation into HSMWorks/HSMExpress:
Once you have a working installation of Solidworks and HSMWorks (or HSMXpress), add this post processor by following these steps:

### Download and extract the post-processor:
* Download the repository as a ZIP file.
* Extract the zip file and copy the file `omio-grbl.cps` into the folder `C:\Program Files\HSMWorks\posts` if you're using HSMWorks or `C:\Program Files\HSMXpress\posts` if you're using HSMXpress.

### Configure HSMWorks/HSMExpress:

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
