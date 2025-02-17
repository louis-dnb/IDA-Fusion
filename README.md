
# IDA-Fusion (Ported to Visual Studio)

## Overview
This project is a port of **IDA-Fusion**, originally designed to work with IDA Pro 9.0, now adapted to be compiled with **Visual Studio** instead of GCC. **IDA-Fusion** is a tool specifically designed to extend the functionality of IDA Pro, making reverse engineering tasks more efficient.

This repository provides the source code and build instructions for using **IDA-Fusion** with IDA Pro 9.0 (version 9.0.240925) in Visual Studio.

This project is based on the original **[IDA-Fusion](https://github.com/senator715/IDA-Fusion/)** repository. All credit goes to the original authors for their work.

## Installation Instructions (No Compilation Required)

If you do not want to compile the project yourself, you can download the latest release and follow these steps:

### 1. Download the Latest Release
Get the latest release [here](https://github.com/louis-dnb/IDA-Fusion/releases) or compile it yourself.

### 2. Copy Plugin Files
Drag **IDA-Fusion.dll** into your IDA installation's **plugins** folder.

### 3. Access the Fusion Menu
Once the plugin is installed, you can access the Fusion menu by:
- Using **Edit > Plugins > Fusion**, or
- Pressing **CTRL + ALT + S** to open the action menu.

## Compilation Instructions

## Prerequisites

- **IDA Pro 9.0** (version 9.0.240925)  
- **Visual Studio** (Recommended: Latest version)
- IDA Pro SDK (installed with IDA Pro)

## Setting Up the Project

### 1. Clone the Repository
First, clone the repository to your local machine:
```bash
git clone https://github.com/louis-dnb/IDA-Fusion.git
```

### 2. Set Up the Project in Visual Studio
1. Open the solution file (`.sln`) in **Visual Studio**.
2. Make sure that the project properties are configured to correctly link with the **IDA SDK**.

### 3. Configure the IDA SDK Paths
In Visual Studio, ensure that the following properties are correctly set to point to your **IDA SDK** installation (typically located in `C:\Program Files\IDA Professional 9.0\sdk`):

#### C/C++ -> General -> Additional Include Directories:
```plaintext
C:\Program Files\IDA Professional 9.0\sdk\include;%(AdditionalIncludeDirectories)
```

#### Linker -> General -> Additional Library Directories:
```plaintext
C:\Program Files\IDA Professional 9.0\sdk\libd_win_vc_64;%(AdditionalLibraryDirectories)
```

### 4. Set Build Configuration
Make sure you build the project in **Release x64** configuration.

To set this:
1. In Visual Studio, go to **Build** -> **Configuration Manager**.
2. Select **Release** and **x64** from the configuration options.

### 5. Build the Project
Once the project properties are configured correctly, you can build the solution by selecting **Build** -> **Build Solution** (or pressing `Ctrl + Shift + B`).

## Contributions
Contributions are welcome! Feel free to submit pull requests or open issues.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
