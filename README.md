# retropie

Repo to store lab used to work with RetroPie. Builds a vm using vagrant with the RetroPie repo (https://retropie.org.uk/) code cloned.

## Status

Coming soon.

## Requirements
1. Vagrant
2. Ansible

## Usage

### In terminal
1. To bring up the vm run:
```bash
vagrant up
```
2. Login to run setup script:
```bash
vagrant ssh [instanceName]
```
3. Run the first time setup script:
```bash
sudo ./git/Re
```

### In virtualbox
1. Login to the vm username & password are retro
2. Launch emulation station and start controller configuration.

At this point it is on the end user to load in systems and ROM's.

## To-Do
Automate guest add-on's.