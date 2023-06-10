# Install requirement

- [Oh my posh](https://ohmyposh.dev/)
- [z](https://www.powershellgallery.com/packages/z/1.1.13)
- [fzf](https://www.powershellgallery.com/packages/z/1.1.13)
- [neovim](https://neovim.io/)
- [PSReadLine](https://github.com/PowerShell/PSReadLine)
- [Terminal-Icons](https://github.com/devblackops/Terminal-Icons)
- [Window Terminal](https://apps.microsoft.com/store/detail/windows-terminal/9N0DX20HK701?hl=vi-vn&gl=vn)
- [Nerd Font](https://www.nerdfonts.com/)

## Install script instruction

1. ##### Install scoop

```
iwr -useb get.scoop.sh | iex
scoop install curl sudo jq
```

2. ##### Install Neovim

```
scoop install neovim gcc
```

3. ##### Install Oh my posh

```
scoop install https://github.com/JanDeDobbeleer/oh-my-posh/releases/latest/download/oh-my-posh.json
```

4. ##### Install Terminal-Icons

```
Install-Module -Name Terminal-Icons -Repository PSGallery -Force
```

5. ##### Install z, PSReadLine, fzf

```
Install-Module -Name z -Force

Install-Module -Name PSReadLine -AllowPrerelease -Scope CurrentUser

scoop install fzf && Install-Module -Name PSFzf -Scope CurrentUser -Force

```

## Setup terminal instruction

1. Install Nerf Font

   1.1 [Page](https://www.nerdfonts.com/)

   1.2 Install the specific font that you want.

   > I'm using `NotoSansMNerdFont-Regular.ttf`

2. Install Window Terminal

   2.1 Open Window Terminal, select `Settings`.

   2.2 In `Startup` options, select `Powershell` as `Default profile`

   2.3 In `Profiles > Powershell > Additional settings`, select `Appearance`.

   2.4 Select Font face that you have install in first step.

3. Setup Profile

   3.1 Create config folder

   ```
   mkdir .config/powershell
   ```

   3.2 Create script for Profile setup

   ```
   nvim $PROFILE.CurrentUserCurrentHost
   ```

   > Copy content of file `Microsoft.PowerShell_profile.ps1` in this repo and paste into your editor

   3.3 Copy theme settings (`mine-theme.omp.json`) to config folder

4. Close and open new terminal. U can see the results now
