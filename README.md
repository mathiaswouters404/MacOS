# My MacOS Installation Guide

## Step 1: Go through the installer

Simply, just finish the installer.

## Step 2: Must change settings

1) Update MacOS
2) Settings --> General --> Software Update --> click the icon next to Automatic updates --> enable 'Install Security Responses and system files'
3) Settings --> Appearance --> enable 'Dark mode'
4) Settings --> Appearance --> change Accent and Highlight colors to color that I want
5) Settings --> Appearance --> Switch Sidebar icon size to 'Small'
6) Settings --> Desktop & Dock --> change Size (smaller) and Magnification 
7) Settings --> Desktop & Dock --> enable 'Minimize windows into application icon'
8) Settings --> Desktop & Dock --> enable 'Automatically hide and show the Dock'
9) Settings --> Desktop & Dock --> disable 'Show recent applications in Dock'
10) Settings --> Desktop & Dock --> disable 'Show suggested and recent apps in Dock'
11) Settings --> Desktop & Dock --> at Desktop & Stage Manager --> disable Show Items On Desktop --> disable Show Items In Stage Manager
12) Settings --> Desktop & Dock --> at Desktop & Stage Manager --> change 'Click wallpaper to reveal desktop' to 'Only in Stage Manager'
13) Settings --> Desktop & Dock --> at Mission Control --> enable 'Group windows by application'
14) Settings --> Trackpad --> enable 'Tap to click'
15) Settings --> Wallpaper --> change to own wallpaper
16) Settings --> Displays --> change 'Use as' to 'More Space'
17) Settings --> Displays --> disable 'Automatically adjust brightness'
18) Settings --> Control Center --> change 'Bluetooth' to 'Show in Menu Bar'
19) Settings --> Control Center --> change 'Sound' to 'Always Show in Menu Bar'
20) Settings --> Control Center --> at Battery enable 'Show Percentage'
21) Settings --> Network --> enable 'Firewall'
22) Settings -->
23) Settings -->
24) Settings -->
25) Settings -->
26) Settings -->
27) Settings -->
28) Settings -->
29) Settings -->
30) Settings -->

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

## Step 5: Commands to execute
### Auto Show/Hide Dock:

keep smooth animation time, but remove delay:
`defaults write com.apple.dock autohide-delay -float 0; killall Dock`

instantly reveal:
`defaults write com.apple.dock autohide-time-modifier -int 0; killall Dock`

restore default behavior:
`defaults delete com.apple.dock autohide-delay; killall Dock`

## Step 6: Homebrew

### Applications
- Firefox
- Arc
- Bitwarden
- Docker (Docker Desktop)
- Terminal (iTerm2 + oh my zsh / warp / ...)
- Logi Options+
- Notion ?? (maybe use web version or not ??)
- Rectangle (window manager) (maybe something else ??)
- AltTab
- Hidden Bar
- Kap (Screen recorder / Screenshot tool)
- Spotify
- Surfshark
- Twingate
- VS Code
- Microsoft Office Suite (Microsoft365)
- nvm (node version manager)
- Git
- Postman
- Raycast
- Figma
- ...

## Step 7: iTerm2 + oh my zsh Setup

### Terminal Setup

...

### CLI Tools
- ...

## Step 8: GitHub Setup

## Step 9: dotfiles Setup

[YouTube Video](https://www.youtube.com/watch?v=GK7zLYAXdDs) --> (Minute: 44:53)

[GitHub Repo](https://github.com/mischavandenburg/dotfiles)

