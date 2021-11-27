# linux-setup
🐧 My personal computer setup guide

## Steps

1. Install linux distro `Manjaro KDE plasma 21.1.6`
2. Partitioning [Partitioning guide](https://atanasrusev.com/2020/04/06/hard-disk-partitioning-during-manjaro-linux-setup/) 
3. Tell pacman to use fast operation
	```bash
	$ sudo pacman-mirrors --fasttrack
	```
4. Update packages
	```bash
	$ sudo pacman -Syyu
	```
5. Enable SSD trim _(Only if you have SSD)_
	```bash
	$ sudo systemctl status fstrim.timer
	
	$ sudo systemctl enable fstrim.timer

	$ sudo systemctl start fstrim.timer
	```
6. Enable `AUR Support` in Pacman
7. Install ttf-ms-fonts from `AUR`
8. Remove orphaned software and packages
9.  Install base-devel
	```bash
	$ pacman -S base-devel -needed
	```
10. Install common apps
    1.  Code - OSS
    2.  VLC
    3.  Steam
    4.  Spotify
    5.  Blender
    6.  Deluge
11. Setup git with new SSH key [Setup guide](https://docs.github.com/en/authentication/connecting-to-github-with-ssh) 
12. Setup ZSH [Intallation guide](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
13. Install Oh-my-zsh
	```bash
	$ sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
	```
14. Install Powerlevel-10k Meslo Nerd Font from `AUR`
15. Setup Powerlevel-10k [Installation guide](https://github.com/romkatv/powerlevel10k)
16. Install Oh-my-zsh plugins
    1.  git
    2.  history-substring-search
    3.  zsh-syntax-highlighting
    4.  zsh-autosuggestions
17. Add some aliases in `.zshrc` file
	```bash
	alias dev="cd ~/home/documents/dev && cd $1"
	alias pro="cd ~/home/documents/projects && cd $1"
	```  
18. Install Golang [Installation guide](https://go.dev/doc/install)
    1.  Add to the path in `.zshrc` file
		```bash
		export PATH=$PATH:$HOME/go/bin
		```
19. Install NodeJS with PNPM
20. Setup Code - OSS
21. Install PostgreSQL with PGAdmin [Installation guide](https://tecadmin.net/how-to-install-postgresql-in-ubuntu-20-04/)
22. Install LAMP [Installation guide](https://www.linuxandubuntu.com/home/install-lamp-on-manjaro)
23. Change KDE Konsole color scheme [KDE Store](https://store.kde.org/browse?cat=462)