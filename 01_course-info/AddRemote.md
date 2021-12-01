# Adding an upstream remote

## Situation: 

You forked a repo and brought a copy down locally. You've done some work and you want to keep it. However - there's a change on the master you want to bring down to your machine. How do you do it?

## Add an upstream remote

[Git Instructions for adding a new remote](https://help.github.com/articles/adding-a-remote/)

**Steps**:
 - From the command line navigate to your local git repository
 - Make sure to backup your current status
 
	```git add . ```
	
	```git commit -m "Message"```
	
	```git push```
- In your browser navigate to the repo you want to pull  from (e.g. class pages)
	- Copy the clone link
	- In the command line add the following command with the clone url
	
	```git add remote upstream <url>```
	
	- You've told the command line the following
		- **git** - From git
		- **add** - we're going to add something
		- **remote** - a new remote
		- **upstream** - It's a conventional name for the repo before your fork. However, you can name this anything you want
		- The **url** you want to link to
		
	- Now you've added your new repo!
	- Let's verify it by running
	
	```git remote -v```
	
	- If you're seeing both your forked repo and the class repo urls next to origin and upstream - then you've succeeded!
	
To get new class information make sure you've first updated your local against your forked repo then running

```git pull upstream master```

You've just told git to fetch and merge any new files from the upstream repo at the master head. 
