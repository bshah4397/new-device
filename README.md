### **Basic commands / softwares / packages for setting up a new dev environment for a new Mac device 💻 😌**

#### 1. Terminal

- ** Xcode**
  ```console
  *** Installation: XCode Select Tools
    Before beginning any other installation simply install the 
    necessary pacakges for mac which are available from XCode 
  
  bshah:~$ xcode-select --install
  ```

- **🐧 Homebrew**
    ```console
    *** Installation: brew
    
    bshah:~$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
    bshah:~$ brew upate
    ```
- **🐧 zsh**
  ```console
  *** Installation: zsh  
    Before using zsh we need to update the system files to make 
    zsh as one of the acceptable shells in a Mac
  
  bshah:~$ brew install zsh
  bshah:~$ brew info zsh # Get the installed location of the installed zsh
  bshah:~$ sudo nano /etc/shells # Add the installed zsh location in the accepted shell's list for your mac
  bshah:~$ echo $SHELL # Should print the location of the zsh shell which is running

  *** Installation: oh-my-zsh
    The DeFacto framework to use with the zsh shell
    
  bshah:~$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
  
  *** Installation: oh-my-zsh Extras
  - Plugins
  
  bshah:~$ git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting # Syntax highlighting
  bshah:~$ clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions # Auto Suggestions
  bshah:~$ brew install autojump # Autojump {j}
  
  - Themes
  
  bshah:~$ git clone https://github.com/romkatv/powerlevel10k.git $ZSH_CUSTOM/themes/powerlevel10k # Powerlevel 10k
  bshah:~$ p10k configure
           (Classic) -> (Unicode) -> (Darkest) -> (No) -> (Angled Seperator)
           (Round Head:Tail) -> (One Line) -> (Compact) -> (Many Icons)
           (Fluent) -> (Yes Transient) -> (Quite Instant Prompt)
  ```
  > The [`~/.zshrc`](https://github.com/bshah4397/new-device/blob/master/zshrc) file is present in the repository for quick copy-paste setup.
  
- **🐧 SSH**
    ```console
    *** Installation: SSH
    
    bshah:~$ mkdir ~/.ssh # Create a directory
    bshah:~$ mkdir ~/.ssh/gitlab # Create a sub-directory for only Git SSH keys
    bshah:~$ cd ~/.ssh/gitlab/
    bshah:~$ ssh-keygen -t rsa -b 4096 -C "bshaxxxxx@gmail.com" # Generate SSH Key
    bshah:~$ cd ~/.ssh/gitlab/id_rsa
    bshah:~$ pbcopy < ~/.ssh/gitlab/id_rsa.pub # Copy the key and paste it into Git SSH Keys
    
    *** Check: SSH Keys Present / Linking Already Present Keys
    
    bshah:~$ ssh-add -l # Check if the idenity exists already or not from all the ssh identities
    bshah:~$ ssh-add ~/.ssh/gitlab/id_rsa # Add / Bind the key if not identity doesn't exist
    bshah:~$ 
    ```
- **🐧 Python**
    ```console
    *** Installation: Python 3.X
    
    export PATH="/usr/local/opt/python/libexec/bin:$PATH" # Add in ~/.zshrc
    
    bshah:~$ brew install python
    bshah:~$ python
    Python 3.X.X # Homebrewe'd Python 3.X
    >>>
    bshah:~$ python2 
    Python 2.X.X # Apple's Python 2.X
    >>>
    ```
    
<hr>

#### 2. Other Apps

- ** iTerm2**
    ```console
    *** Installation: iTerm2
    
    bshah:~$ brew cask install iterm2
    
    *** Customization: 
    - Appearance > Theme > Minimal
    - Profile > Colors > Color Presets > Pastels (Dark Background)
      Profile > Default > Text > MesloLGS NF | 12 / 13
      Profile > Default > Keys > Presets > Natural Text Editing
          
    ```

- **🐧 Node**
    ```console
    *** Installation: Node Version Manager
    
    bshah:~$ brew install nvm 
    bshah:~$ mkdir ~/.nvm # Only if file does not exists
    bshah:~$ echo "source $(brew --prefix nvm)/nvm.sh" >> .zhsrc # Lazy Load Global Initialization of NVM
    bshah:~$ nvm -v # Latest version of NVM installed
    
    bshah:~$ nvm install node # "node" is an alias for the latest version
    bshah:~$ nvm install 10.19.0 # Install v10.19.0
    
    bshah:~$ nvm use node # Only if you have more than one version of node installed
    
    
          
    ```
    
- ** Other Important Applications** 
    ```console
    *** Installation: Google Chrome
    Cross-platform web browser
    
    bshah:~$ brew cask install google-chrome 
    
    *** Extensions
    - OneTab
    - JSON Viewer 
    - AdBlocker
    - React Developer Tools
    
    
    *** Installation: VS Code
    Open-source code editor
    
    bshah:~$ brew cask install visual-studio-code
    
    *** Installation: Docker
    App to build and share containerized applications and microservices
    
    bshah:~$ brew cask install docker
    
    *** Installation: Postman
    Collaboration platform for API development
    
    bshah:~$ brew cask install postman
    
    *** Installation: Slack
    Team communication and collaboration software
    
    bshah:~$ brew cask install slack
    
    *** Installation: VLC
    Open-source cross-platform multimedia player
    
    bshah:~$ brew cask install 
    
    *** Installation: Alfred
    Application launcher and productivity software
    
    bshah:~$ brew cask install alfred
    
    *** Installation: TeamViewer
    Remote access and connectivity software focused on security
    
    bshah:~$ brew cask install teamviewer
    
    *** Installation: Dozer
    Hide menu bar icons on macOS
    
    bshah:~$ brew cask install dozer
    
    *** Installation: 
    
    
    bshah:~$ brew cask install 
    
    *** Installation: Spectacle
    Move and resize windows with ease
    
    bshah:~$ brew cask install spectacle  
    
    ---------------------------------------------------------
    
    *** Installation: Micro 
    A terminal-based text editor that aims to be easy to use 
    and intuitive, while also taking advantage of the capabilities 
    of modern terminals.
    
    bshah:~$ brew install micro
    
    ```
    
