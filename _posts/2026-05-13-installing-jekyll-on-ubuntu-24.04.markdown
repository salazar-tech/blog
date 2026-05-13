---
layout: post
title: "Installing Jekyll on Ubuntu 24.04"
tag: information-technology
---
Installing Jekyll on Ubuntu 24.04 requires setting up the Ruby environment first. Since Ubuntu 24.04 is a Long Term Support (LTS) release, it’s best to install through the official repositories for stability.

## Update System Packages
Ensure your package database is current:

```bash
sudo apt update && sudo apt upgrade -y
```
## Install Ruby and Dependencies
Jekyll requires Ruby and several development tools to compile "native extensions" (software written in C that Ruby uses).

```bash
sudo apt install ruby-full build-essential zlib1g-dev
```
## Configure the Ruby Gem Path
To avoid using sudo every time you install a Ruby gem (which is a security best practice), configure a local "gems" directory in your home folder.

Add these lines to your .bashrc file:

```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
## Install Jekyll and Bundler
Now that your environment is set up, install Jekyll and Bundler (which manages project-specific dependencies):

```bash
gem install jekyll bundler
```
## Verify Installation
Check that Jekyll is installed and accessible:

```bash
jekyll -v
```
