# VS Code dev containers with Oh my zsh (Powerlevel10k theme)

- [VS Code dev containers with Oh my zsh (Powerlevel10k theme)](#vs-code-dev-containers-with-oh-my-zsh-powerlevel10k-theme)
  - [Description](#description)
  - [Setup](#setup)
    - [NOTE about step 2](#note-about-step-2)
  - [Features](#features)
 
## Description

A sample project to let you try VS Code container (Node JS Image) with oh-my-zsh, powerlevel10k theme

## Setup

1. Clone the resitory
2. Install VS Code `Remote - Containers` Plugin
3. Setup Icons Support (Not required if already using Powerlevel10k theme)
   1. Download a font of your choice from <https://www.nerdfonts.com/>
   2. Install those font
4. Set the Terminal Font in VS code
   1. Go to Settings (JSON)
   2. Add the line `"terminal.integrated.fontFamily": "<Your Installed Font>"`
   3. eg. `"terminal.integrated.fontFamily": "FiraCode NF"`
5. Click on Remote Window Icon in bottom left
6. Reopen in Container

### NOTE about step 2

- Nerd font is required because default fonts do not support Icons and Glyphicons. It is simply an extension to normal fonts with those extra features. You need to looked for Nerd font version of your existing font. If this step is skipped, icons will not appeaar properly in terminal
- Defualt user is  root user

## Features

- Customised container for Node JS Container
- All [oh-my-zsh](https://github.com/ohmyzsh/ohmyzsh) related settings can be modified at [.devcontainer -> .zshrc](.devcontainer/.zshrc)
- All [powerlevel10k](https://github.com/romkatv/powerlevel10k) settings can be modified at [.devcontainer -> .p10k.zsh](.devcontainer/.p10k.zsh)
- `powerlevel10k` First time setup has been disabled by default
- To install any oh-my-zsh plugin, add the git clone command to [.devcontainer -> Dockerfile](.devcontainer/Dockerfile)
- Rebuild Container after changing any of these settings


## Root and Not Root

### Non Root
- Uncomment USER node in Dockerfile

  
### Root
- Comment USER node in Dockerfile

### NOTE
- Global packages cannot be instaled as non root user
- Add them to dockerfile instead

