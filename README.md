<h1 align="center">helpmecode.github.io</h1>

## Pushing a project to GitHub

GitHub is a web-based platform used for project version control and codebase hosting. GitHub uses Git, a widely-used version control system. GitLab and Bitbucket are similar tools.

Using GitHub is a prerequisite of most of the tutorials on this site, so it is helpful to learn to use it. In this tutorial, I’ll show you how to push a project to GitHub.

##Prerequisites

To follow this tutorial, a few things are required:

  *  Basic knowledge of Git
  *  Git installed on your system
  *  A GitHub account

With GitHub ready to go, we can start the tutorial.

## Setting Up

To keep things simple, we’ll use a single HTML file. You can review the HTML file here.

There are a few ways to get the HTML file we need.

 * Copy the code in the gist (linked above) into an ```index.html``` file.
 * Go to this link, then click Download this one page web-profile.
 * Use Terminal to go to the project folder you want to use and run:
```bash 
wget https://raw.githubusercontent.com/CIRCLECI-GWP/profile/master/index.html
```

However you choose get the HTML, you will have one file, ```index.html```, at the root of your directory.

For the rest of the tutorial, we will use Terminal to run commands. Unless instructed otherwise, run commands at the root level of your project directory.

### Initializing Git

Because we created our file locally, we need to push it to GitHub to store it there. The first step is initializing Git.

Run:

```bash 
git init
```
The git init command turns your directory into a new Git Repository.

### Adding files

With Git initialized, we need to mark it so that it is included in the next commit. This process is also called staging.

Run:

```bash 
git add .
```

### Committing files

Our file is now marked and ready for its first commit. A commit is a snapshot of the history of changes to the file.

Run:
```bash
git commit -m "Add index.html"
```

The text following -m is the commit message. It is a human friendly reminder about what changes are in the commit.

# Pushing to GitHub

Pushing uploads all your local commits to the remote repository. This makes the changes in your file available to people you are working with. There are two parts to this process:

 - [x] Creating a repository
 - [x] Pushing the project

### Creating a GitHub repository

In your browser, go to **github.com** and log in if you need to. Click the plus sign icon at the top right of the page. Then select __New Repository__.

Enter a name, then click **Create Repository**. I have used the name *new-repository* for this tutorial. We will be using this name later on, so make a note of it.

There you have it, a sparkling new repository. If this is your first one, **congratulations!** You have reached a programming milestone.

Stay on the Create Repository page to complete the next step.

# Pushing the project to GitHub

So far in our project folder we have just one file, and we have committed the changes we made to it. The next step is to push these changes to GitHub. Our project is in ‘new-repository’, which we just created, so we can push to an existing repository.

Click the ```clipboard``` icon to copy the three commands shown in the “push an existing repository from the command line’ section. Paste them in your Terminal and press **ENTER** to execute them.

__Note:__ *Replace the username shown in the code with your GitHub username.*

```bash
git remote add origin https://github.com/NdagiStanley/new-repository.git
git branch -M main
git push -u origin main
```

After running these commands, reload the browser page. Our ```index.html``` file is now listed in the online repository.

You can make more updates to the repository by running these commands in order:

```bash
git add .
git commit -m "Commit message"
git push origin main
```

Replace the sample message with a descriptive one of your own. If you are working on a branch other than ```main```, replace that with the name of the branch you are using.

# Conclusion

In this tutorial, you pushed an online git repository to GitHub. Getting comfortable with Git and GitHub will let you move on to the next step of setting up a CircleCi project based on your GitHub repository. GitHub and other Git-based version control systems are widely used. Understanding them can be a key addition to your developer’s skill-set toolkit.

About Stanley: From a young age, Stanley tinkered with electronics and building things with tech. His work involves data, the web, and IoT. Stemming from his lifelong love of DIY, he’s on a personal journey of invoking the builder within and teaching others along the way. He cares about how technology affects society and seeks collaborations with others who are working to create positive impact.
