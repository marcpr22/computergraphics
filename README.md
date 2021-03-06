# Computer Graphics

The framework provided is compatible with all operating systems.
The recommended C++ IDEs are the following:

* MS Visual Studio 2015 Community edition (Windows)
* MS Visual Studio 2017 Community edition (Windows)
* XCode (Mac)
* Visual Studio Code (Any platform)
* Qt Open Source (Any platform)

Detailed installation information can be seen below.

## MS Visual Studio 2015 Community edition (Windows)

MS Visual Studio 2015 can be downloaded from [here](https://my.visualstudio.com/Downloads?q=visual%20studio%202015&wt.mc_id=o~msft~vscom~older-downloads). Make sure you select all packages
related to C++.

After the installation you just need to open the file *visual.sln* located in the *visual* folder.

## MS Visual Studio 2017 Community edition (Windows)

MS Visual Studio 2017 can be downloaded from [here](https://visualstudio.microsoft.com/thank-you-downloading-visual-studio/?sku=Community&rel=15#).
Make sure you select all packages related to C++.

In addition you need to install *CMake* which can be downloaded from [here](https://github.com/Kitware/CMake/releases/download/v3.13.2/cmake-3.13.2-win64-x64.msi).

Once you have all required software go to this file folder and run this on a windows console:

```console
mkdir build
cd build
cmake -G "Visual Studio 15" ../.
```

## XCode (Mac)

You need XCode installed in your system and also Homebrew to install the missing libraries and
*cmake*. To install Homebrew open a terminal and run this command:

```console
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

Continue by installing *cmake* and the missing libraries using this command:

```console
brew install cmake
brew install sdl2
```

Finally create the XCode project by going to this file folder and run these commands:

```console
mkdir build && cd build
cmake -G "Xcode" ..
```

The XCode project will be located into the *build* directory.

If this process leads to cmake errors, run this command an try again:

```console
sudo xcode-select --reset
```

## Visual Studio Code (Any platform)

If you need a more light weight IDEs which can be used in any platform (included Linux), this is
your better option.

Visual Studio Code can be downloaded for each platform in [here](https://code.visualstudio.com/download).

### Requirements on Windows

Windows do not need any further requirement.

### Requirements on Mac

**It is not recommended since there is a bug in one the the needed extensions, that prevents
starting the debugger, use XCode instead.**

Once the ide is installed, on **Mac** it is necessary to first open the application and and press
**Cmd+Shift+P**, then type *"shell command"* and select *"Shell Command: Install 'code' command in
PATH"*. Then it is also necessary to install the following pakcages:

Homebrew to install the missing libraries and
*cmake*. To install Homebrew open a terminal and run this command:

```console
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install cmake
brew install sdl2
```

### Requirements on Linux

If you are using **linux** you have to install the following packages:

```console
sudo apt-get install -y libsdl2-dev libglew-dev freeglut3-dev
```

### Configuring VSCode

After the VSCode and the requirements for each platform are installed, the following extensions
are needed to work with C++ code:

```console
code --install-extension ms-vscode.cpptools
code --install-extension twxs.cmake
code --install-extension vector-of-bool.cmake-tools
code --install-extension austin.code-gnu-global
```

Finally open the folder containing this file.

## Qt Open Source (Any platform)

Qt Open Source can be downloaded from [here](https://www.qt.io/download-qt-installer). Once it is
installed you have to install the same packages that you seen in the previous section. After that
you have to create a new cmake project.
