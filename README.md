Vagrant installer for cpp craft cources
===

Requirements 
---
To install requirements you'll need to download [Vagrant installer](http://www.vagrantup.com/downloads.html) from the site. Also fetch and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) for your version of operating system. The project is developed for any kind of morden popular operating system (Windows, Mac OS, Linux), still the most friendly environment for the project is Unix systems. I run this project with following configuration:
- Mac OS X 10.9.2
- VirtualBox 4.3.8
- Vagrant 1.3.5

Installation
---
After you installed Vagrant and VirtualBox go project folder and run commands
```
git submodule add -f <cpp-craft-git-repo-url> cpp-craft
vagran up
```
Notes:
- `<cpp-craft-git-repo-url>` is link to your fork of cpp craft repo (for instance in my case it is `git@github.com:allomov/cpp_craft_0314.git`).
- you can use `VM_MEMORY` and `VM_CORES` variables in [Vagrantfile](https://github.com/allomov/cpp-craft-vagrant-installer/blob/master/Vagrantfile) to adopt project to your hardware.

Usage
---
After `vagran up` was finished without errors you can run `vagrant ssh` to log in to the virtual machine. You'll have your project in `~/cpp-craft` folder. After you've made all changes you can login VM, go to `cpp-craft` folder in your repo and push it to github.

Enjoy your code!