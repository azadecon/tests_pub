---
title: "making a project wiki website"
author: "arshad azad"
date: "April 11, 2022"
---


## Q1. Making the project website.


### Tools/services used to make the website.

 

1. We use `git` to control and manage the Project wiki, for `git` could help maintain individual workstreams and the associated sub-workstreams and all the future additions.

2. `Github` for storage and `Github-pages` to host the website.

3. `Hugo` provides a simple way to make a website.

Using `git`, I would initiate a repository on a provider such as **GitHub**. It provides the option of keeping the repository public or private, which could be helpful per the type and stage of the project. As and when we start new projects, it is possible to create another repository. This provides a way to keep track of all the new and old data. This also provides a systematic way to version control codes and other related files including the content of the website.


Since, **GitHub** already has all the files associated with the project, all that remains is to point to it when we want to refer to a particular file/resource on our Project wiki. This is where website building tool **Hugo** comes into play. It is important that we make a simple, editable, transparent, portable, and a future proof website. In conjugation with **GitHub** and simple markdown we could create a website. All the posts on the website could be written in a simple text ediotor. No worries about the alignment being off or anything like that, the template takes care of all that. All the past, present, and future posts are going to be consistent, aesthetically of course. Setting up a `Git` hosted website also provides the portability to other providers including but not limited to **Wordpress** and **Netlify**.

### Process

### Step1: 

Create a repository "website" on github. (This is a different repository to host the contents of the website over and above the other repositories holding the project files.)

### Step2: 

Make a website using `Hugo`. `Hugo` provides an option to choose from several templates. These templates can be easily modified as per our project and aesthetic requirements.

	1. `hugo new site website`
#### Select a theme from [here](https://themes.gohugo.io/)
	1. `cd website/themes`
	2. git clone git@github.com:goodroot/hugo-classic.git
	3. cp -a hugo-classic/exampleSite/. ../
	4. cd .. && hugo server

These steps create a website on local machine. It can be viewed on the browser but it is still not on the internet. It is a good idea to preview the website before publishing it.	


### Step3: 
Push the website on `Github`.




#### Steps to prepare "website" to be pushed on `GitHub`.
	0. cd website/
	1. git init
	2. git add .
	3. git commit -m "message"
	4. git remote add origin git@github.com:user/website.git
	5. git push -u origin master

Create yet another repository "website.github.io" on github. This is where our actual website will live with all its interconnected links and structre.

#### Steps to prepare "website.github.io"
	1. git clone git@github.com:user/website.github.io.git
	2. cd website
	3. hugo -d ../website.github.io
	4. cd ../website.github.io
	2. git add .
	3. git commit -m "message"
	4. git remote add origin git@github.com:user/website.github.io
	5. git push
	
So far we have pushed only a structural website on the internet. The site is only a demo site as of now, with random stuffs which came with the theme. After updating home/other page and making all the changes following steps would make our website a usable one.

With `Hugo` new posts could be initiate with command.[^Markdown]


	1. `Hugo new content/posts/new_post.md`.
	
[^Markdown]: Markdown is super editable. Links to the repositories or any website link could be easily added in the website. This is how we do it. `[hyperlink name](www.resource-on-internet.com)`.

#### This syncs changes made on the website with github. They have not been deployed yet.

	1. `cd /website`
	2. `git add .`
	3. `git commit -m "msg"`
	4. `git push`
	
#### ReBuilding site

	1. `hugo -d ../website.github.io`

#### Deploying the channged site
	
	1. `cd ../website.github.io`
	2. `git add .`
	3. `git commit -m "msg"`
	4. `git push`
	

The website is live!








# Optional Question
Due to paucity of time I could not create a specific website. However I have linked my own website. I have created it the way outlined here.


## [Link](https://azadecon.github.io) to the demo website.
