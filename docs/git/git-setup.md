# Installing Git on Linux

This guide provides step-by-step instructions for installing Git on various Linux distributions.

## Prerequisites

- A user account with sudo privileges.
- An internet connection.

## Installation Steps

### 1. Update Package Index

Before installing Git, update the package index to ensure you have the latest information on available packages.

``` bash
sudo apt update
```

### 2. Install Git

#### For Debian-based distributions (e.g., Ubuntu):

``` bash
sudo apt install git
```

#### For Red Hat-based distributions (e.g., CentOS, Fedora):

``` bash
sudo dnf install git`
```

or for older versions:

``` bash
sudo yum install git
```

#### For SUSE-based distributions (e.g., openSUSE):

``` bash
sudo zypper install git
```

### 3. Verify the Installation

After the installation is complete, verify that Git is installed correctly by checking its version.

``` bash
git --version
```

You should see output similar to:

``` bash
git version 2.x.x
```
![Terminal Screenshot](../attachements/git-version-terminal-screenshot.png)


## Configuration

### 1. Set Your Username

``` bash
git config --global user.name "Your Name"
```

### 2. Set Your Email

``` bash
git config --global user.email "your.email@example.com"
``` 
