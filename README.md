# OmioCNC-Postprocessor
If you've got an OmioCNC machine with the [EPL Offline Controller](https://www.omiocnc.com/epl-4f-control-system/) (commonly known as The Orange Box), the postprocessor in this repository will help when generating your `.nc` files.
There are a couple of quirks with the way the controller interprets the `.nc` files which means the standard grbl postprocessor doesn't work properly.
Fortunately, this customised grbl post generation script appears to solve those issues.


## Installation:
Once you have a working installation of Solidworks and HSMWorks, add this post processor by following these steps:

* Download the repository as a ZIP file.
* Extract the zip file and copy the file `omio-grbl.cps` into the folder `C:\Program Files\HSMWorks\posts`.
