
# Techjoomla Documentation Site

Steps to contribute documentation to the Techjoomla Site.

## Git Fork Setup on local machine

1. Fork the repo <a href="https://github.com/techjoomla/techjoomla.github.io" target="_blank">Techjoomla Documentation Repo</a>
2. Git clone your fork to your machine. Command Syntax - ```git clone fork-link```
3. Add remote upstream by command ```git remote add upstream git@github.com:techjoomla/techjoomla.github.io.git```
4. Check upstream with command ```git remote -v```
5. Make filemode off in config file. File Path - ```/techjoomla.github.io.git/.git/config``` . Make sure you can see the .git hidden folder by ```Ctrl + h```

## Installing requirements

1. Install Ruby - ```sudo apt-get install ruby-full```.
2. Check Ruby installed correctly by command - ```ruby -v```. It should be ```minimum 2.1.0```
3. Install Bundler - ```sudo apt-get install bundler```.
4. Check Bundler installed correctly by command - ```bundle -v```. It should be ```minimum 1.15.3```
5. Go to the root folder of project. i.e. ```/techjoomla.github.io```
6. Install Rubygems - ```sudo bundle install```.

## Basic Usage

### Adding a New Post

1. Start the development server with command ```bundle exec jekyll serve```
2. It will give you the link where you can see the changes.
3. Inside _post folder create a new md file format ```YYYY-MM-DD-filename.md```
4. Open the same file you created and add front matter 
     ``` 
        ---
        date: 2017-01-15
        title: Post Title
        description: Post Description
        categories:
          - CategoryName
        type: Document
        --- 
     ```
5. This will add a section on homepage with Category name and a post under it. The post will be generated with url - ```domainname.com/categoryname/filename```
6. Add below the front matter your content to be added on that post. To know markdown follow [this link](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)

### Adding a Video Post

1. Inside _post folder create a new md file format ```YYYY-MM-DD-filename.md```
2. Open the same file you created and add front matter 
     ``` 
        ---
        date: 2017-01-15
        id: youtube-video-id
        title: Post Title
        description: Post Description
        categories:
          - CategoryName
        type: Video
        --- 
     ```
 
### Adding a Menu Item

1. Inside _data folder open ```navigation.yml``` file.
2. Add Menu item - 
    ```
      - name: Link Name
        link: /link-url/
    ```
## Understanding Folder Structure

| **Folder Name**  | Description                                               |
|:----------------:|:---------------------------------------------------------:|
| **css**          | Do not edit any file here. This is autogenerated by SASS  |
| **_data**        | Contains Navigation and Footer data.                      |
| **images**       | Put your all images here.                                 |
| **_includes**    | This folder contains common reusable html structures.     |
| **js**           | Include Js here                                           |
| **_layouts**     | This folder contains the layouts / templates              |
| **_posts**       | Add posts inside this folder                              |
| **_sass**        | Add CSS here                                              |
| **_site**        | This is your output html                                  |
| **config.yml**   |                                                           |

## Precations

1. Never ever write in css file directly. Add it in scss/sass folder files. Otherwise you may loose the changes.
