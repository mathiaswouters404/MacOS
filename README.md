# My MacOS Installation Guide

## Step 1: Go through the installer

Simply, just finish the installer.

## Step 2: Must change settings

1) Update MacOS
2) Settings --> Network --> enable 'Firewall'
3) Settings --> General --> Software Update --> click the icon next to Automatic updates --> enable 'Install Security Responses and system files'
4) Settings --> Appearance --> enable 'Dark mode'
5) Settings --> Appearance --> change Accent and Highlight colors to color that I want
6) Settings --> Appearance --> Switch Sidebar icon size to 'Small'
7) Settings --> Accessibility --> Pointer Control --> Trackpad Options --> enable 'Use trackpad for dragging'
8) Settings --> Control Center --> change 'Bluetooth' to 'Show in Menu Bar'
9) Settings --> Control Center --> change 'Sound' to 'Always Show in Menu Bar'
10) Settings --> Control Center --> at Battery enable 'Show Percentage'
11) Settings --> Desktop & Dock --> change Size (smaller) and Magnification 
12) Settings --> Desktop & Dock --> enable 'Minimize windows into application icon'
13) Settings --> Desktop & Dock --> enable 'Automatically hide and show the Dock'
14) Settings --> Desktop & Dock --> disable 'Show recent applications in Dock'
15) Settings --> Desktop & Dock --> disable 'Show suggested and recent apps in Dock'
16) Settings --> Desktop & Dock --> at Desktop & Stage Manager --> disable Show Items On Desktop --> disable Show Items In Stage Manager
17) Settings --> Desktop & Dock --> at Desktop & Stage Manager --> change 'Click wallpaper to reveal desktop' to 'Only in Stage Manager'
18) Settings --> Desktop & Dock --> at Mission Control --> enable 'Group windows by application'
19) Settings --> Displays --> change 'Use as' to 'More Space'
20) Settings --> Displays --> disable 'Automatically adjust brightness'
21) Settings --> Wallpaper --> change to own wallpaper
22) Settings --> Trackpad --> enable 'Tap to click'

## Step 3: Other Settings

1) Right click on the desktop (NOT in finder) --> Click 'Use Stacks'
2) Remove all unnecessary apps from the dock
3) Organize the apps in Launchpad

## Step 4: Finder Settings

1) Open finder --> Click on Desktop --> Right click --> Show View Options --> Change 'Sort By:' to 'Snap to Grid' --> Click 'Use as Defaults'
2) Open finder --> View --> enable 'Show Path Bar'
3) Open finder --> View --> enable 'Show Status Bar'
4) Open finder --> Settings --> General --> change 'New Finder windows show:' to 'username folder'
5) Open finder --> Settings --> General --> disable 'Open folders in tabs instead of new windows'
6) Open finder --> Settings --> Sidebar --> modify the sidebar how I want
7) Open finder --> Settings --> Advanced --> enable 'Show all filename extensions'
8) Open finder --> Settings --> Advanced --> at Keep folders on top --> enable 'In windows when sorting by name'
9) Open finder --> Settings --> Advanced --> at Keep folders on top --> enable 'On Desktop'
10) Open finder --> Settings --> Advanced --> change 'When performing a search' to 'Search the Current Folder'
11) Open finder --> in root folder (username folder) --> make a 'Developer' folder
12) Open finder --> Change the sidebar order
13) Open finder --> Add NAS storage

## Step 5: Commands to execute
### Auto Show/Hide Dock:

keep smooth animation time, but remove delay:
`defaults write com.apple.dock autohide-delay -float 0; killall Dock`

instantly reveal:
`defaults write com.apple.dock autohide-time-modifier -int 0; killall Dock`

restore default behavior:
`defaults delete com.apple.dock autohide-delay; killall Dock`

## Step 6: Applications

### Xcode Command Line Tools & Clone this repo
- Xcode Command Line Tools include git and other things

- Install Xcode Command Line Tools: `xcode-select --install`
- Clone this repo: `git clone https://github.com/mathiaswouters404/macos-install`

### Homebrew:
- Install:
`/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
- Execute the 2 commands given to you in the terminal to add homebrew to your path
- Update brew: `brew update`

#### Install applications:
- `cd macos-install`
- `xargs brew install < packages.txt`
- `xargs -I {} brew install --cask {} < applications.txt`

#### Install nvm (node.js):
- Install nvm with the command in this [link](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating)
- `nvm install node`

## Step 7: iTerm2 + Oh-My-Zsh Setup

### Install Oh-My-Zsh:
`sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"`

### Install PowerLevel10k:
- `git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k`
- `nano ~/.zshrc`
- Change the value of `ZSH_THEME` to `"powerlevel10k/powerlevel10k"`

### PowerLevel10k configuration:
- `source ~/.zshrc`
- `y`
- Quit iTerm2
- Open iTerm2 --> If config wizard don't shows up run following cmd `p10k configure`
- Follow the config wizard

### iTerm2 Preferences:
- Open: "Command + ,"
- Profiles --> Keys --> Key Mappings --> Presets... --> Natural Text Editing
- Profiles --> Colors --> Color Presets... --> Import... --> coolnight.itermcolors

### Install ZSH Plugins:
- `git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions`
- `git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting`
- `nano ~/.zshrc` --> change `plugins=(git)` to `plugins=(git zsh-autosuggestions zsh-syntax-highlighting)`
- `source ~/.zshrc`

## Step 8: GitHub Setup

### Config Git
- `git config --global user.name "you name"`
- `git config --global user.email your_email@example.com`

### GitHub Generate SSH Key
- `ssh-keygen -t ed25519 -C "your_email@example.com"`
- Save to default location
- Enter passphrase
- `eval "$(ssh-agent -s)"`
- `nano ~/.ssh/config`
- ```
  Host github.com
    AddKeysToAgent yes
    UseKeychain yes
    IdentityFile ~/.ssh/id_ed25519
  ``` 
- `ssh-add --apple-use-keychain ~/.ssh/id_ed25519`

### GitHub Add SSH Key
- `pbcopy < ~/.ssh/id_ed25519.pub`
- Go to GitHub website --> Settings --> SSH and GPG keys --> New SSH key or Add SSH key
- Give it a title and paste the key in the Key box

### Test SSH Connection
- `ssh -T git@github.com`
- Verify that the resulting message contains your username

## Step 9: dotfiles Setup

[YouTube Video](https://www.youtube.com/watch?v=GK7zLYAXdDs) --> (Minute: 44:53)

[GitHub Repo](https://github.com/mischavandenburg/dotfiles)

