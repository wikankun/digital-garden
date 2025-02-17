---
title: 2024-10-27 After Install Ubuntu
description: 
tags:
  - tutorial
  - ubuntu
  - guide
date: 2024-10-27
---

# Things I do after installing Ubuntu

1. Setup dock position & dock autohide

2. Update and upgrade all software

    ```
    sudo apt update
    sudo apt upgrade
    ```

3. Install tree, curl, wget, git

    ```
    sudo apt install tree curl wget git
    ```

4. Setup git email & git name

    ```
    git config --global user.email "your@email.com"
    git config --global user.name "Your Name"
    ```

5. Install zsh

    ```
    sudo apt install zsh
    ```

6. Install oh my zsh

    ```
    sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
    ```

7. Install zsh theme (powerlevel10k)

    - Clone the repository
        ```
        git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
        ```
    - Set `ZSH_THEME="powerlevel10k/powerlevel10k"` in `~/.zshrc`

8.  Install font mesloLGS NF

    - Download and install MesloLGS NF font
        ```
        curl -OL https://github.com/romkatv/powerlevel10k-media/raw/master/MesloLGS%20NF%20Regular.ttf
        ```
    - Change terminal font
		Open Terminal → Preferences and click on the selected profile under Profiles. Check Custom font under Text Appearance and select MesloLGS NF Regular

9.  Install gogh color scheme. My favorite color scheme is VSCode Dark+ (so it matches with my VSCode)

    ```
    sudo apt-get install dconf-cli uuid-runtime
    bash -c "$(wget -qO- https://git.io/vQgMr)"
    ```

10. Add zsh plugins by editing `.zshrc`

    ```
    plugins=(git docker docker-compose git-auto-fetch)
    ```

After sucessfully installed Ubuntu on your new machine, now let's explore about apps we need to install [[2024-10-28-ubuntu-apps]]
