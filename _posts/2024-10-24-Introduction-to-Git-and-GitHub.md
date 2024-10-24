---
title:  "Git n Github 01: Introduction to Git and GitHub"
search: true
categories: 
  - Git n Github
last_modified_at: 2024-10-24T08:06:00-05:00
---

Understand what is Git and GitHub?

# What is Git and Github?
New hi
![Git and Github](images/Git-n-Github/git-github.png){:height="70%" width="70%"}

<div style="text-align: center"><img src="../assets/images/Git-n-Github/git-github.png" alt="Git n Github" width="350px" ></div>

{% capture fig_img %}
![Foo]({{ "../assets/images/Git-n-Github/git-github.png" | relative_url }})
{% endcapture %}



- Git:
  - A **distributed version control system (VCS)** that tracking changes in source code during software development. 
  - It allows you to manage your codebase efficiently, collaborate with others, and revert to previous versions if needed.

- GitHub:
  - web-based Git repository hosting service, which offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features. 

|  | Git | Github |
|---|---|---|
| 1 | software | service |
| 2 | command-line interface (CLI) | graphical user interface (GUI)|
| 3 | installed locally on the system | hosted on the web |
| 4 | manage source code history | hosting service for Git repositories |


# Git vs. Other Version Control Systems

# Basic Git Workflow
<div style="text-align: center"><img src="../assets/images/Git-n-Github/git-workflow.png" alt="Git n Github" width="350px"></div>

- Working directory: where we edit files
- Staging area: a temporary location where files are kept for the next commit
- Local repository: contains the code that has been committed
- Remote repository: the remote server that stores the code

## Git workflow when teamwork
<div style="text-align: center;"><img src="../assets/images/Git-n-Github/git-workflow-teamwork.png" alt="Git n Github" width="350px"></div>

# Git basics
## Preparation
Download and install Git from official Git website: 
<a href = "https://git-scm.com/downloads"> Git SCM </a>  
Configure Git:
```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

## Basic commands
- **Create a new directory**: This will be the root of your project.  
- **Initialize a Git repository**: Navigate to the directory and run:
```
git init
```

- **Create a file**
- **Add change files to the staging area**
```
git add <filename>: add files to the staging area
```
```
git add .: add all changed files to the staging area 
```
- **Commit changes**: Create a snapshot of the staged changes  
When you make a commit, Git stores a commit object that contains a pointer to the snapshot of the content you staged. This object also contains the author’s name and email address, the message that you typed
```
git commit -m "<commit message>"
```
- **View commit history**: Use git log to view the commit history.
```
git log
```

# References 

<a href = "https://www.geeksforgeeks.org/difference-between-git-and-github">Difference Between Git and GitHub</a>  - Geeksforgeeks  
<a href = "https://blog.bytebytego.com/i/95179881/how-does-git-work"> How does git work? </a> - ByteByteGo