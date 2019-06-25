# MacBook Setup



**First, Create an Apple ID**




## Make a bootable MacOS install USB drive

1. Download a macOS installer for [macOS Mojave](https://support.apple.com/kb/HT201475) 
2. Set USB volume name to MyVolume
3. ```
   sudo /Applications/Install\ macOS\ Mojave.app/Contents/Resources/createinstallmedia --volume /Volumes/MyVolume
   ```


**Using the installer:**

1. Connect the bootable installer to a compatible Mac. 
2. Use Startup Manager or Startup Disk preferences to select  the bootable installer as the startup disk, then start up from it.
   1. Press and hold the Option key immediately after turning on or restarting your Mac.
   2. Release the Option key when you see the Startup Manager window.
   3. Select your startup disk, then click the arrow under its icon, or press Return. 
3. Connect to Wi-Fi using the Wi-Fi menu in the menu bar. 
4. Select Install macOS (or Install OS X) from the Utilities window, then click Continue and follow the onscreen instructions.




## Update to Mojave

-*App Store > Updates > Update*
  If error:``` *Error: You may not install to this volume because it is currently being encrypted- ```
  - Check encryption progress:
    - *System Preferences > Security & Privacy > File vault*
  - When done, Install *App Cleaner*  & *Clean My Mac




## Install HomeBrew

1. Install Xcode command line utilities: 

   `xcode-select --install`

2. install *HomeBrew*:
   - ```/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"```
   - `brew update`
   - Usage: 
     - `brew search <term>`
     - `brew install <brew>`



## Install CLI Tools

#### Bash

1. Check bash version for 4.x `bash -v`
   - `brew install bash`
2. Check again `which bash`
3. Make bash default shell:
   - `sudo vi /etc/shells`
   - add the path `/user/local/bin/bash`
   - comment out the other paths
   - change to new shell: `chsh -s /usr/local/bin/bash`
4. Customize bash profile:
   - make profile: `touch .bash_profile`

#### iTerm2

`brew cask install iterm2`

#### ZSH

`brew install zsh`

- `chsh -s $(which zsh)`

- [Oh my zsh](https://github.com/robbyrussell/oh-my-zsh): 

  `zsh -c “$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"`

**oh my zsh plugins:**

- Enable plugins, edit vi ~/.zshrc`
  - zsh-syntax-highlighting
  - zsh-autosuggestions



## Install Node.js & NPM

1. Install NVM
   `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash`
2. `nvm install stable`
3. Install global packages:
   ```
   npm install -g tldr typescript @vue/cli vuepress @angular/cli eslint gitbook/cli lodash
   ```
   
   

## Install Software

#### SDKMAN:

`curl -s "https://get.sdkman.io" | bash`

- Java SDK: 

  	`sdk install java`

- gradle: 

  	`sdk install gradle`

#### Miscellaneous:

```brew install 
brew install \
java \
gradle \
mysql \
mongodb \
elasticsearch
```



#### Dev Tools:

```
brew cask install \     
brew cask install \
mysqlworkbench \     
docker \     
gitkraken \     
postman \     
android-studio \     
jetbrains-toolbox \     
sublime-text \     
visual-studio-code \
atom
```



## Install Generic Software 

```
brew cask install \    
gimp \  
viber \
slack \
discord \
google-chrome \
firefox \
firefox-developer-edition \
brave \
microsoft-office \
spotify \
vlc \
typora \
p7zip \
audacity \
sketch
```



#### Browser Addons

- LastPass
- Grammarly
- Color Picker
- LiveReload
- uBlock Origin
- privacy badger 
- oneTab
- JSONViewer
- Vue devtools
- honey

  

## Change System Preferences 

#### Trackpad:

 `System Preferences > Trackpad > Scroll & Zoom`
 Uncheck scroll direction: Natural (It doesn’t feel natural for me) 

#### Dock:
 `System Preferences > Dock`

 - Change the size to small and turn on magnification
 - Remove all icons from the dock you don't use

#### Avatar:
`System Preferences > Users & Groups > Edit Avatar`

#### Theme:
`System  Preferences > General > Appearance`



## Configure Finder

**Locations**

- Add Macintosh HD to locations so can always get to the root hard drive
- Home /Users/<name>
- screenshots (configure screenshot utility to save here)  
  - open screenshot > options > other location 

**A few tips in finder**

- cmd+shift+h (takes you home)
- cmd . (show hidden files and folders)
