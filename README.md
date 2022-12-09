# UOX3
[![License: GPL v2](https://img.shields.io/badge/License-GPL%20v2-blue.svg)](https://www.gnu.org/licenses/old-licenses/gpl-2.0.en.html) 

**Ultima Offline eXperiment 3** - Allows one to run their own, custom UO shards.

Supported UO Client versions: **~4.0.0p** to **~7.0.91.15** (with encryption removed by [ClassicUO](https://www.classicuo.eu), [Razor](https://github.com/msturgill/razor/releases) or similar tools).  
---

# How to compile UOX3...
UOX3 supports Integrated Development Environment(IDE) building for Visual Studio 2022, and XCode.  CMake is available for command line building.  
## Step 1: Setting up an environment  
### Acquire the compiler and build tools  
	-) **Windows**  Visual Studio 2022 ([Free Community edition](https://visualstudio.microsoft.com/downloads/))  
	-) **macOS**  Via the App store,download XCode.  
	-) **Linux**  Debian based distributions execute: `sudo apt install build-essentials`  
### Aquire Git
	-) **Windows or macOS**  Download [GitHub Desktop](https://desktop.github.com/)  
	-) **Linux**  Debian based distributions execute: `sudo apt install git`  
	
### Acquire CMake (if using command line build generation)  
	-) **Windows** CMake is part of the Visual Studio IDE, nothing more is needed  
	-) **macOS** Download and install [CMake](https://cmake.org/download/)  
	-) **Linux** Debian based sitrubitons execute: `sudo apt install cmake`  
## Step 2: Cloning the software  
	-) **GitHub Desktop**  
		-) Run GitHub Desktop and click **File->Clone Repository** from the menu.  
		-) Click the **URL** tab, enter **https://github.com/UOX3DevTeam/UOX3.git**, then provide a local path for where you want the UOX3 git repository cloned on your drive.   
		-) Hit the **Clone** button!  
	-) **Command Line**  
		-) `git clone https://github.com/UOX3DevTeam/UOX3.git`  
  			-)If you'd rather grab another branch of the git repository, like the **develop** branch where most updates get pushed first before being merged into the master branch, you can use the following command *after* completing the previous step: `git checkout develop`  
## Step 3: Compile UOX3  
	-) **Windows**  Open the UOX3\ide\VS2022\uox3\uox3.sln file, select build.  
	-) **macOS**  Open the UOX3/ide/XCode/uox3/uox3.xcworkspace.  Select build.  
	-) **Linux**  
		-) Enter the following:  
			-) `mkdir build`  
			-) `cd build`  
			-) `cmake ../server -DCMAKE_BUILD_TYPE=Release `  
			-) `cmake --build . --config Release`  


The binary/executable will be located:  
	-) **Windows**  UOX3\ide\vs2022\uox3\x64\Release\uox3.exe  
	-) **macOS**  UOX3\ide\XCode\uox3\Build\Products\Release\uox3  
	-) **Linux**  UOX3/build/uox3  
	

# Setting up the shard's directory
## Creating directories and acquiring the data
	1. Create a directory for your shard (e.g. `mkdir MyShard`)
	2. Change to that directory (e.g. `cd MyShard`)
	3. Create the following directories in MyShard
		-) accounts  
		-) archives  
		-) books  
		-) logs  
		-) msgboards  
		-) shared
	4. Clone from git the following repositories into *MyShard* directory  
		-)  dictionaries  
		-)  dfndata  
		-)  jscripts  
	5. Copy the uox.ini file from the UOX3 directory into the *MyShard* directory
	6. Copy the **uox3** executable/binary into the UOX3 directory  

## Edit the *MyShard/uox.ini* file as needed.  
# Starting your shard  
From the *MyShard* directory run the **uox3** executable/binary.
	