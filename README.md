# GitWrap
Windows Wrapper for Linux git executable.

Windows Subsystem for Linux is pretty awesome, but managing two separate git environment is not, especially if you use SSH keys. So, here is a little workaround that lets you call git from the WSL environment through a Windows executable.

GitWrap is currently a Proof Of Concept solution and is in no way complete or reliable. It has been tested with Android Studio and seems to work pretty well when set up correctly.

## Requirements
- Windows Subsystem for Linux must be installed. 
- Git should be installed in the Linux environment.
- Supports x64 variant of Windows only. 

## Installation
Download the latest GitWrap release, extract and save the executable anywhere you want. Then configure your IDE's git executable path and make it point to GitWrap.exe. It should now be using git from your Linux Subsystem on Windows 10.

It should work with other IDE's but I've only tested and verified functionality with Android Studio.

## Known Issues
- Using GitWrap manually as a command line tool is a bit cumbersome. Commiting files is pretty much impossible since GitWrap cant interface with external editors for commit messages etc. You should use GitWrap with IDE's and other applications that integrate with git or interact with git directly through WSL.
- With the initial version of Windows Subsystem for Linux it was impossible to pipe output from a Linux command directly to a Windows application. Gitwrap worked around this by piping output to a temporary file and reading the output from there. Because of this, Windows 10 Creators Update is required for GitWrap version 0.2.0.0 and newer. If you're still on an older version of Windows 10 with WSL you can use the older GitWrap releases or use the legacy branch.

If you encounter any other issues, bugs or limitations please report them!
