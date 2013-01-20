# Participant Configuration

## Install VirtualBox

If you haven't done so yet, [install VirtualBox](https://www.virtualbox.org/wiki/Downloads).
You only need to install the proper package in the section "VirtualBox platform packages"
for the RailsBridge.

Start VirtualBox, then go into the settings

## Prepare to run the VM

### Network

- Start VirtualBox
- Open Preferences / Network
- Add a host-only network
- Edit it, and change the IPv4 address to `10.10.10.1`

### Import the VM

- Download the VM
- Double-click the .ova file to import it to VirtualBox
- Accept the defaults
- Start your VM!

## Your Virtual Machine

Here are your credentials on the Virtual Machine

- Username: railsbridge
- Password: ruby rocks

## Configure git

```shell
git config --global user.name "Your Actual Name"
git config --global user.email "Your Actual Email"
```

Note: Use the same email address for heroku, git, github, and ssh.

### Verify settings

```shell
git config --get user.name
git config --get user.email
```

Should return respectively your name and email.

# Configure Heroku, SSH, then 

Most of the work of installing tools has already been done.
You only need to continue the process from
[here](http://installfest.railsbridge.org/installfest/create_a_heroku_account#big_checkbox_434).


# Tips for Ubuntu

## General

- To run arbitrary programs, click on the Ubuntu logo (top of left bar), then type
the name.
- To install additional programs, run "Ubuntu Software Centre"

## Terminal

- Copy / Paste: Shift-Ctrl-C and Shift-Ctrl-V
- New tab: Shift-Ctrl-T
- Clear the window, run the command "clear"
