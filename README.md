# Linode-Setup
A place for my personal notes on setting up a Linode server for various situations.

## Basic setup
- ***ssh into the server*** - `ssh root@your.server.ip` If you are on Windows, you can just click **Launch LISH Console** from the server page on the Linode website.
- ***Run the following commands*** - Wait for each command to finish before moving to the next one. you may be prompted to press y if you forget the -y flag
- ***Update your system*** - `apt update`
- ***Upgrade your system (optional)*** - `apt full-upgrade -y`
- ***Create dev user*** - `useradd -m dev`
- ***Create user password*** `passwd dev` enter password twice
- ***Add user to sudo group*** `usermod -a -G sudo dev`
- ***Reboot the server*** - `reboot` wait a few minutes after this before doing the next step
- ***ssh into the server as new user*** - `ssh dev@your.server.ip`
- ***change shell to bash (if needed)*** - `chsh -s /usr/bin/bash`
- ***Install additional software as needed*** - `sudo apt install tmux ufw git build-essential -y`
- ***Allow ssh through firewall*** - `sudo ufw allow ssh`
- ***Enable firewall*** - `sudo ufw enable`
