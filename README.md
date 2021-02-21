# Kulbir_Website

We will be using Hugo to generate the static website. The Theme that we will be using is Academic kickstarter.

## Installing Hugo

### STEP1: Install brew:
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Add the following line to your .zshrc:
```
eval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)

#you can also use the following command to add the line above to your .zshrc or .bashrc
echo '\neval $(/home/linuxbrew/.linuxbrew/bin/brew shellenv)' >> /home/kulbir/.zshrc

# this command will make sure that Homebrew is added to your PATH in ~/.zshrc 
```
Install Homebrew dependencies:
```
sudo apt-get install build-essential
```
Install GCC:
```
brew install gcc
```

### STEP 2: Install Hugo using Brew
Refer: https://gohugo.io/getting-started/installing/#install-hugo-with-brew 
```
brew install hugo
```
After hugo is installed, type ```hugo version``` to check the hugo version.
You should get the following in terminal:
```
Hugo Static Site Generator v0.80.0/extended linux/amd64 BuildDate: unknown
```
This confirms that Hugo has been installed correctly.













