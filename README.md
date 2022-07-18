# Kulbir_Website

We will be using Hugo to generate the static website. The Theme that we will be using is Academic kickstarter.
Reference video: https://www.youtube.com/watch?v=X4KzvWMKYaY by Mathieu Besançon.

## Installing Hugo and Go
For help on using tar to unzip .tar.gz files: https://websiteforstudents.com/how-to-use-the-tar-command-to-create-and-extract-tar-gz-files-on-ubuntu-16-04-18-04/

I do not recommend using brew or snap to install either go or hugo-extended because in that case the packages cannot find each other. There are also additional sourcing problems. JUST USE THE BINARY FILE.


### STEP 1: Install "Hugo Extended" using its binary file
Refer: https://gohugo.io/getting-started/installing/#install-hugo-from-tarball
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
For ubuntu, refer https://golangdocs.com/install-go-linux:
```
#install go
cd /usr/local
sudo tar -C /usr/local/ -xzf ~/Downloads/go1.18.4.linux-amd64.tar.gz  

#add path
sudo nano $HOME/.profile  
# add the following line to the end of .profile and then save
export PATH=$PATH:/usr/local/go/bin
source .profile


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


### STEP 4: Check website locally
Serve the website locally using:
```
cd ~/your github repo
hugo server --disableFastRender
```
Go to the link provided in terminal. Crtl+click on it.
This is useful to quickly check if the changes you make result in an error or work as expected.
when you make any changes, the changes are also accomodated in the website automatically. You do not need to restart your local web server.

When you have accumulated enough changes, you can push the changes to your github repo and deploy the website using netlify. 

### STEP 5: Modify contents of config folder
1. title: Kulbir Singh Ahluwalia # Website name
2. baseurl: 'https://kulbir-ahluwalia.github.io/' # Website URL
3. copyright: '© 2022 Kulbir Singh Ahluwalia' # Footer text, e.g. '© {year} Me'


### STEP 6: Using GitHub pages
Make your (github username).github.io repository to host your website.
Refer: https://pages.github.com/

```
rm -rf public #remove public folder if it exists 
git submodule add -f -b master https://github.com/kulbir-ahluwalia/kulbir-ahluwalia.github.io.git public
```
The public folder has your static website.

### STEP 7: Generate your website
In this step, we generate the website and push all chnages to GitHub. 
```
hugo #to generate your static website in the public folder
git add -A
git commit -m "added public folder and the static website in it"
git push
```
Go to your github-username.github.io to see your newly hosted website. 

# Editing the website

### STEP 1: Using hugo new command
```
hugo new content/post/welcome.md 
```
Edit welcome.md to add new content. 
draft: false means that the new content is ready to be published on the website.
draft:true means it will not be published. 
```
hugo server -D   #to see website with drafts included
```
You can now add your content in markdown in the .md file. It also supports LaTeX. Images, PDFs, GIFs or other files hsould be in the static folder.

### STEP 2: Creating a new post
```
#To see all possible options:
hugo new --help 

#To make a new post in /posts:
hugo new content/post/welcome.md 
```
Then you can edit the contents of this welcome.md to suite your needs.
1. You can add LaTeX code: 
```The mass-energy equivalence is described by the famous equation
\begin{equation}
E=mc^2
\end{equation}
```
2. You can create a foler called "static_images" in the "static" folder and then add pictures from that folder using any one of:
 ```
![test_picture](/static_images/Dr_Tony_Stark.jpg)

#the following line adds a caption as well:
{{<figure library="true" src="/static_images/Dr_Tony_Stark.jpg" title="Test_picture" lightbox="true">}}
```

### STEP 3: Creating a new publication
```
pip3 install -U academic 
code content/publication/refs.bib

#the following commands makes a new folder for each one of your bibtex entries:
academic import --bibtex content/publication/refs.bib
```


