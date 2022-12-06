

## Downloading, Installing, and using HASE

Using one of the download-able HASE models requires you:
to be able to run HASE
to have your own copy of the model files
The download-able version of HASE includes both the code for HASE and an installer that works with Linux, Windows, MACs and 32 and 64-bit Intel MACs.

The latest version of HASE is version 3.8. Version 3.8:


### Requirements

Prior to downloading and installing HASE, please ensure that your system satisfies the following requirements:
Operating System - any of:
- A Desktop Linux Operating System
- OSX
- Microsoft Windows Vista/7/8/10/11

System Requirements:
- Java Runtime Environment 1.5 or newer
- Compiler Requirements (one of)
- GCC (g++)
-Microsoft Visual Studio

Environment Requirements for Linux/OSX:
- To check that a symbolic link exists to java, type:  java -version in a Terminal window
    the result should be:  java version "1.x.x.x"
- To check that a symbolic link exists to GCC, use:  g++ --version
the result should be:  g++ (GCC) 3.x.x.xxxxxxxxx (OS information)
- If either of these links does not exist, but the required versions of Java and GCC are installed on your system, then before continuing, make links to them using the 'alias' command in your .brc file, or by setting symbolic links.

Environment Requirements for Windows:
- Check that java binaries are accessible (set in the PATH environmental variable) by typing the following command in a Command Prompt window:
 java -version
the result should be:  java version "1.x.x.x"

Check that PATH includes an entry pointing to Visual Studio (e.g. to VS140COMNTOOLS)

### Addition Notes (OSX)

For OSX g++ comes with XCode. XCode can be obtained free of charge from App Store if it didn't come with the OS installation. In XCode Preferences select Downloads > Components > Command Line Tools > Install

### Downloads

The following link can be used to download the latest version of HASE 3:

https://github.com/HASE-Group/hase_iii_releases/blob/trunk/Setup_HASE_3.8.0.5.jar

### Installation

HASE is available in the form of a jar file that includes its own installer. The most recent version (June 2020) is 3.8.

To install HASE-III, either double click on the .jar file to start the installer (if supported by the operating system of the target machine), or execute the following from a terminal:

    java -jar Setup_HASE_3.8.0.1.jar

Download the latest installer into an appropriate directory.

Enter directory containing downloaded installer: 

    cd /Directory_Containing_Jar_File/

If you have root access runn the installer as root:

    sudo java -jar Setup_HASE_3.8.0.1.jar

Follow the installer instructions, selecting 'Install for Everyone' on the option page.

If you do not have root access:

Run the installer:   java -jar Setup_HASE_3.8.0.1.jar

Follow the installer instructions, selecting Select 'Install for Just Me' in the installation options. Make sure you choose an appropriate installation directory (e.g. not /opt in MAC OS X). After the installer finishes in this mode, you will have to make your own alias to /HaseInstallDirectory/bin/Hase to be able to run Hase (e.g. in .bash_profile).

### Model Files

A collection of "official" models are provided in the https://github.com/HASE-Group/models.git repository along with associated documentation.


Each model is a git sub-module therefore when cloning this repository with git the --recurse-submodules should be used. Alternatively individual models can be cloned from individual model repositories.

### Running HASE3

Type:   

    Hase&

HASE-III will default its open dialog box to the directory from which it is run.

To use the model, move to the subdirectory/folder for the model and start up HASE. The file menu or the left most icon in the HASE window can be used to open a selection window and the project is loaded by selecting <model_name>.edl. Then compile the project using the Build Project option in the Project menu (or the build icon).

To run the simulation, use the Simulate option in the Project menu (or the run icon). During the simulation, HASE writes a trace file into a Results subdirectory (model_name.sim). When the simulation stops, load the trace file using the Load Trace File option in the Project menu (or the clock icon). When the tracefile is loaded, the animation buttons will light up. Using these buttons you can play the animation, stop it, single step it, re-wind it, etc.

Selecting the parameters tab in the Project Inspector panel allows changes in the values of entity parameters to be observed during simulation. These include register and memory contents, for example. The parameter display of each entity can dragged out of the main display into a separate window either by clicking on the double lines at the left of the relevant section of the parameter panel or by left clicking on the entity's icon whilst holding down the shift key. If the window is closed, it re-docks with the main display.

## Documentation 

A User Guide for HASE can be accessed via the Help command in the Menu Bar (select Index). This User Guide is also available on the HASE website at HASE User Guide. The latter will generally be more up to date, since updating the Guide in the HASE application requires a new release of HASE itself.

### Disclaimers, Etc

- The Help facility is still under construction; the Hase++ section in particular is incomplete.
- There are still a few bugs in the HASE code that can sometimes throw java errors (e.g. when using the Help facility) - just close HASE and start again.
- Some files for some of the models contain some redundant code left over from development.
- In case of difficulties, please send email to David Dolman or Roland Ibbett and we'll try to help.