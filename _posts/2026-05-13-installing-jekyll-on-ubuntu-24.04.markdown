---
layout: post
title: "Installing Jekyll on Ubuntu 24.04"
tag: information-technology
---
Setting up Jekyll is the first step toward launching your professional website. We will start by installing Ruby, the engine that makes Jekyll run. Because Ubuntu 24.04 is a stable system, this process is straightforward and reliable.
### 1. Refresh Your System
First, let's make sure your computer’s software list is up to date. This ensures everything installs smoothly.
```bash
sudo apt update && sudo apt upgrade -y
```
### 2. Install the Core Tools
Jekyll needs Ruby and a few "behind-the-scenes" tools to help it build your site. Think of these as the essential ingredients.
```bash
sudo apt install ruby-full build-essential zlib1g-dev
```
### 3. Set Up Your Personal Folder
To keep your system secure and organized, we’ll tell your computer to save website tools in a personal folder rather than a restricted system area.
Run these commands to update your settings:
```bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```
### 4. Install Jekyll and Bundler
Now you are ready to install Jekyll itself, along with Bundler (a tool that helps manage your website's specific features).
```bash
gem install jekyll bundler
```
### 5. Check Your Work
Finally, let's verify that everything is ready for you to start building. Run this command to see your Jekyll version:
```bash
jekyll -v
```