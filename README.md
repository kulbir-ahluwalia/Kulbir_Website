# Kulbir_Website

We will be using Hugo to generate the static website. The Theme that we will be using is Academic kickstarter.

## Installing Hugo and Go
For help on using tar to unzip .tar.gz files: https://websiteforstudents.com/how-to-use-the-tar-command-to-create-and-extract-tar-gz-files-on-ubuntu-16-04-18-04/

I do not recommend using brew or snap to install either go or hugo-extended because in that case the packages cannot find each other. There are also additional sourcing problems.


### STEP 1: Install Hugo using its binary file
Refer: https://gohugo.io/getting-started/installing/#install-hugo-with-brew 
```
cd /usr/local/bin
sudo tar -xvzf ~/Downloads/hugo_extended_0.92.0_Linux-64bit.tar.gz
#to verify
./hugo version
```
After hugo is installed, type ```hugo version``` to check the hugo version.
You should get the following in terminal:
```
hugo v0.92.0-B3549403+extended linux/amd64 BuildDate=2022-01-12T08:23:18Z VendorInfo=gohugoio

```
This confirms that Hugo has been installed correctly.


### STEP 2: Install go using its binary file
For ubuntu, refer:
```
https://golangdocs.com/install-go-linux


#install go
cd /usr/local
sudo tar -xvzf ~/Downloads/go1.17.6.linux-amd64.tar.gz 

#to verify
go version

#to see installation directory of go
which go

```
### STEP 3: Choose your theme from Wowchemy + Setup netlify

Choose theme here: https://wowchemy.com/hugo-themes/ 
Once you have connected your GitHub account to the Netlify theme, download the corresponding GitHub repo. Then:

```
To initialize theme of your website:
git submodule update --init --recursive
```
Documentation for wowchemy: https://wowchemy.com/docs/ 








