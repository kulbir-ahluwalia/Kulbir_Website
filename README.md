# Kulbir_Website

We will be using Hugo to generate the static website.

## Installing Hugo

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

















