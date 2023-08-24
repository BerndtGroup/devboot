# devboot

# Purpose
tl;dr: Auto Bulk Software Installs for Dev Workstations via [Winget Configuration]([url](https://learn.microsoft.com/en-us/windows/package-manager/configuration/)) and/or [Dev Home]([url](https://learn.microsoft.com/en-us/windows/dev-home/setup)) app

Microsoft announced a nice new way of doing desired state configuration (DSC) for workstations via pretty simple YAML code/configs - especially for dev systems - at Build, called winget configuration and in tests it's pretty cool. In other words, it can install a list of commonly needed development software with a few clicks in a new app from MSFT called Dev Home or a command from a terminal. 

We also can call it from Dev Box (Windows development workstation in Azure accessed via Remote Desktop, etc) confguration which was also announced at Build and is in private preview now. 

I set up this repo with configs for all of this and worked out some issues and I think it works well. 

You can run the config from the command line pretty easily, but we could also add that to a setup script for this whole thing, too since there's a few steps to being able to use this since it's in preview right now. 

Alternatively, users could install the new Dev Home app from Windows Store, then add their GitHub account, clone the repo in the app (along with a list of other repos in bulk if desired), and use the Machine Configuration > Configuration File option there to run the winget config with a GUI. 

This could/should be very useful to help save probably hours per developer reinstalling software for the when workstations needed to be reset/reimaged or for new machine setups. I will write up some simple instructions for the Dev Home method and share those and the command line method in the Usage section below soon. 

# Usage

## Scripted, one-liner Winget Configuration Setup and Run (coming soon)

## Manual Winget Configuration Setup and Run
1. Install the latest winget "-preview" version from https://aka.ms/getwingetpreview
2. Enable the winget experimental feature "Configuration" with the brief steps at https://learn.microsoft.com/en-us/windows/package-manager/configuration/#enable-the-winget-configuration-experimental-configuration-preview-feature
3. Clone devboot repo
4. Run winget configure -f .winget\configuration.dsc.yaml --verbose from repo root
5. If you run into issues, you can quickly abandon this method and do a manual install of all software and only have spent 5 minutes trying to save a few hours. :)

# Software Suggestions, Ideas
Please make software installation suggestions and other ideas for devboot in the [Ideas Discussion]([url](https://github.com/BerndtGroup/devboot/discussions/categories/ideas)https://github.com/BerndtGroup/devboot/discussions/categories/ideas)
