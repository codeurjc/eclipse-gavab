# eclipse-gavab
Eclipse distribution for education

## Synopsis

This project provides an [Eclipse Oomph](https://projects.eclipse.org/proposals/oomph) setup to create a standalone/preconfigured Eclipse IDE with support for various programming languages. In particular, the resulting installation provides support for the following programming languages.

* Java
* C/C++
* Ruby
* Haskell
* Pascal

To achieve this, the following plugin versions are installed by the setup:

* [CDT 8.5](http://www.eclipse.org/cdt/) - C/C++ plugin support for Eclipse
* [DLTK 5.x Ruby](http://www.eclipse.org/dltk/) - Ruby plugin support for Eclipse
* [EclipseFP 0.10](https://github.com/tcrespog/eclipsefp/tree/eclipsefp0.10) - Haskell support for Eclipse
* [Pascaline](https://github.com/sidelab-urjc/pascaline) - Pascal support for Eclipse
* [IDEConfigurator](https://github.com/tcrespog/IDEConfigurator) - Plugin to configure the IDE allowing standalone behavior. It unzips the required tools and connects each tool with its corresponding plugin.

And the following tool versions required by the plugins to work are shipped along with the setup:

* [MinGW](http://tdm-gcc.tdragon.net/)
* [Ruby 1.9.3](http://rubyinstaller.org/)
* [GHC 7.8.3](https://www.haskell.org/ghc/)
* [FPC 2.6.4](http://www.freepascal.org/)

## Installation
###Installing Oomph Installer

* Download and install [JRE](http://download.eclipse.org/oomph/jre/) >= 1.7 required for Oomph Eclipse Installer to run.
* Download the [Oomph Eclipse Installer](https://wiki.eclipse.org/Eclipse_Installer).
 
###Preparing the setup

* Download each prepackaged tool from each one of these links and put them all inside the working directory (along with the .setup and .jar files).
	* JRE: https://www.dropbox.com/s/ibz4zo96gyw6wae/jre.zip?dl=1
	* MinGW: https://www.dropbox.com/s/6h5vt99v2lyxhyc/mingw.zip?dl=1
	* Ruby: https://www.dropbox.com/s/d6g0fo318apl6pv/ruby.zip?dl=1
	* GHC: https://www.dropbox.com/s/r0bpwvxw5b0ga9t/ghc.zip?dl=1
	* FPC: https://www.dropbox.com/s/imzs6kc4b68ulqe/fpc.zip?dl=1

	![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/folder.png "Content ready")
	
* Run the *prepare.jar* file, this application adjusts the path where each tool is located on the OomphSetup.setup file, this way the Eclipse Installer can copy the tools on the installation path.
You can check after the run that the paths were effectively changed inside the OomphSetup.setup file.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/setupReady.png "Setup ready")

###Performing the installation

* Run the Eclipse Installer executable and switch to advanced mode via the popup menu.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/basic.png "Basic mode")
    
* On the advanced installation window: choose the IDE for Java Developers product and the version.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/advanced.png "Advanced mode")
    
* On the setup selection page: click the plus symbol on the upper left side to add our local custom setup selecting the file OomphSetup.setup.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/selection1.png "Setup selection")
    
    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/selection2.png "Setup selection")
    
* On the installation variables page:
    * Installation location rule: "Installed in a uniquely-named folder within the root install folder"
    * Root install folder: choose your preferred path
    * Installation folder name: eclipse
    * Workspace location rule: "Located in the specified absolute folder location"
    * Workspace location: choose your preferred path
    * Target platform: None

 ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/locations.png "Locations")
 
* On the confirmation page: finish the wizard, you may be prompted with some dialogs which you should accept during the installation process.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/confirm.png "Confirm")

* Close the finish dialog once everything is completed.

* Once the installation is finished and Eclipse is opened for the first time, the IDEConfigurator plugin may take some time to do its work. You can inspect the .log file inside the .metadata directory of the workspace to check if everything is finished.

    ![alt text](https://raw.githubusercontent.com/tcrespog/eclipse-gavab/static/screenshots/log.png "Finished work")

* Now you are ready to use your IDE.
