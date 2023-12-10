# Kali Ansible

## Table of Contents
1. [Project Overview](#project-overview)
2. [Roles](#roles)
   1. [Packages](#packages)
   2. [Terminal](#terminal)
   3. [Tmux](#tmux)
   4. [Transfers](#transfers)
3. [Galaxy](#galaxy)
4. [Getting Started](#getting-started)
   1. [Prerequisites](#prerequisites)
   2. [Installation](#installation)
5. [Contributing](#contributing)
6. [Usage](#usage)
7. [License](#license)
8. [Acknowledgements](#acknowledgements)

## Project Overview

These Ansible Playbooks are used to configure my kali VM the way that I like it. I use these in tandem with kali-packer in order to create my kali virtual machines totally hands free

## Roles

I have broken these playbooks up into roles because it feels cleaner to me

### Packages

These are, obviously, packages I like using in kali via apt. I also make some home directores, and install obsidian as it's only available through a downloaded binary
- this can also be used as a template for whatever you might want to install

### Terminal

This section is for configuring my terminal. I have a pretty custom setup so this gets a little involved. I install oh-my-zsh along with the .p10k.zsh file, fonts, a konsolerc file, and the zshrc file (I've just put the default kali rc file in this repo)

### Tmux 

I'm a huge tmux fan, so I also have a playbook for that. This is relatively simple as I just download oh my zsh, make the symbolic link specified in the install script, and copy in my config file (again using just the default here)

### Transfers

Transfers is used for bringing over any other files I like using. In my case I copy over:
- AutoKey scripts
- Pictures (wallpapers and icons)
- Burp Suite config
- hotkey configs

## Galaxy

I leverage ansible galaxy in order to install vscode and burp suite. These are both community made and allow for a quick installation of both pieces of software. This is supplied in `galaxy.yml` as that is where packer looks for ansible galaxy configurations

## Getting Started

### Prerequisites
For this, you are going to need ansible installed on the host system
- In this case we are using ansible locally, rather than to manage other systems

### Installation

Clone this repo with: `git clone git@github.com:rob0tster/kali-ansible.git`

## Contributing

I welcome any contributions! If you'd like to contribute to the project, please follow these guidelines:

1. Fork the repository
2. Create a new branch for your feature or bug fix
3. Make your changes
4. Submit a pull request

We appreciate your help in making this project better!

## Usage
1. run `ansible-playbook <path-to-playbook.yml>`

## License 
This project is licensed under the [MIT License](LICENSE.md) - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgements
- [Ansible](https://www.ansible.com/) is incredibly useful for automating your sysadmin workflows. 
- Huge shoutout to gantsign for [ansible-role-visual-studio-code](https://github.com/gantsign/ansible-role-visual-studio-code)
- Huge shoutout to iesplin for [ansible-role-burpsuite](https://github.com/iesplin/ansible-role-burpsuite)