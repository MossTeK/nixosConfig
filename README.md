# NIXOS on QEMU/KVM Installation Script

This repository provides an installation script for deploying NIXOS on QEMU/KVM. The script serves as a template for configuring NIXOS as a "server." The intention is not to use the configuration as is, but to fork the repository and customize it for the specific service(s) you plan to host. The `configuration.nix` file is configured with minimal settings, and it is important to replace the default user "teK" with your own.

## Default Included Packages

The default set of packages included in the installation script are as follows:

- vim
- wget
- neofetch
- git
- lf

Feel free to modify the `configuration.nix` file to include or exclude packages according to your requirements.

## Installation Procedure

The installation script partitions the disk with a basic setup designed for legacy boot, not UEFI. The partitioning includes:

- 8GB swap partition
- EXT4 for the main partition

## Instructions

1. Fork this repository to your own account.
2. Customize the `configuration.nix` file according to your server requirements.
3. Replace the default user "tek" with your desired username.
4. You will need to update this.

## Usage

You will want to curl this script as Nix dosent ship with Git, you\'ll want to
`curl https://raw.githubusercontent.com/MossTeK/nixConfigTemplate/main/install.sh >> install.sh && chmod +x ./install.sh`
