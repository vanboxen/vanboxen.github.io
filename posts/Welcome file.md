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
This is the folder structure after the installation. I put in bold the most used ones or at least the ones that we are going to use.
 
├ **archetypes**
├ **content**
├ data
├ layouts
├ resources
├ static
├ **themes**
└── **config.***

| Folder / File | Purpose  |
|--|--|
| archetypes | store your md (markdown) file templates |
| content | where your static pages and posts are live |
| themes | themes installation folder |
| config.* | the config file of your site |

The config file is the most important one and based on your theme you will have to use a *.toml file or *.yaml.

Reading the theme installation is really important and mostly all the customization that you can perform can we found there.

> Later another folder will be created called "public" where the webpage code resides and the one that is pushed into the hosting sites.

## Themes
There are a good bunch of themes on the official webpage of HUGO so feel free to use and test all of them.

Basically, you have to download them to the theme folder and then point the config file to the correct theme. Finally, build again HUGO (I will explain these later). For example for the PaperMod theme execute the next commands:

    cd my_website
    git clone https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod --depth=1
 

> if you were anxious like me and you already have git running on the folder just do a "git submodule add" instead of clone on the last command.

PaperMod needs a yaml file and by default, after the instalation, you have a config.toml file so save it as backup and create a new one with the info from theme itself. 

    cd my_website
    mv config.yaml config.yaml.bkp
    touch config.yaml

Then paste the basic config lines inside the previous created file.

    baseURL: "https://examplesite.com/"
    title: ExampleSite
    paginate: 5
    theme: PaperMod

The main difference with toml and yaml is the structure so you will get a lot of errors when you build the site with HUGO after.

At this point, it's worth it to execute HUGO for the first time to see if you already have errors on your config file.

    hugo # that simple!
    
The **public** folder will be created too now since the command is a kind of compilation command so it creates everything needed to run your site on internet. This will throw some lines on your monitor with errors if something went wrong or with this table if everything is fine:

Start building sites …

|  | EN |
|--|--|
| Pages | 10 |
| Paginator pages | 0 |
| Non-page files | 0 |
| Static files  | 2 |
| Processed images | 0 |
| Aliases | 3 |
| Sitemaps | 1 |
| Cleaned | 0 |

> In case of errors, google is your friend! But usually is related with a miss-typo inside the config file or something that maybe is obsolete for your version of HUGO.

## First post! Getting big
To post just execute:

    cd my_site
    hugo new content/posts/first-post.md
    
Go to the file with your favorite text editor and you will see a couple of lines already there. This comes by default and if you want to edit them later you can place a file inside the **archetypes** folder with the info that you want like tags, content, etc. Really depends on how are you going to use the page.

Also, by default comes "draft = true" which means that you are creating a file that is a draft and is not going to be published. Either you can remove, comment or change it to true to make the page available.

Execute HUGO again to avoid config issues.

    hugo


## Running HUGO locally

 We have our page configured and our first post ready to be shared. Let's test HUGO locally and see how the pages looks like.

    hugo server

On the prompt, you will see the page that you need to reach your website.

    http://localhost:1313

 ## Publish your site
 
I used Github Pages to put this blog online. It's simple and I like the fact that I can handle everything with git from different devices if needed.
 
Execute HUGO one more time

    hugo

> always before your are going to push changes on your website

The last part is to create the repository on Github and start git on your **public** website folder.


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
eyJoaXN0b3J5IjpbLTUxNTE2NDYwMSwtMjEzNjgzODQxNCw2Mj
U4MDgzOTcsLTEyMzU3NTIwOTZdfQ==
-->