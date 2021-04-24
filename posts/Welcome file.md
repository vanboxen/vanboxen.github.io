# HowTO install HUGO

## Must have
brew
git

## Installing HUGO
You will need first to have brew installed on your device so make sure that is up and running. Then from linux/mac just open the terminal and install HUGO.

    brew install hugo

If everything was fine just check it with:

    hugo version

Now a days is common to have git preinstalled by default. Anyway, if you need to check if the package is already there there then:

    git --version

Otherwise, use your favorite package manager to install it if it's not already there. For example:

    zypper install git

Hurray! We have everything that we need.

## Let's first create our site locally
Now that we have everything installed is time to setup our site locally. Later on, I will explain how to move it outside your device.

Go to whatever folder you want and create a specific one for the site.

    cd Desktop ; hugo new site my_website

> A new folder called my_website will be created on the Desktop

Then you will have a nice prompt telling you where to download themes and how to do some customization, etc.
 
 ## Folder structure

my_website
 
├── archetypes
├── content
├── data
├── layouts
├── resources
├── static
├── themes
└── config.*

# Most common topics

- rpi
- open source packages
- monitoring
- NAS
- NFS 
- SMB
- Sync the phone on the NAS
- **Big etc!**

## Learning curve

I really expect to have a huge learning curve just because I've never done such a thing and also because I'm a real "test and failure" person!
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTE2NDUwMTM5MywtMjEzNjgzODQxNCw2Mj
U4MDgzOTcsLTEyMzU3NTIwOTZdfQ==
-->