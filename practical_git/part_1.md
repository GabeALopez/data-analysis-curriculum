#  What Is Git and Github and Why Use Them?

Git, what is it? Git is a version control software and used widely by many programmers throughout the world. But what is a version control software really? A version control software is a type of software that help keep track of changes between versions of a set of code/project. The reasoning for keeping track of versions is to not only understand what has changed between versions of your code but also in the case of an emergency you can roll back to a perviously known good version. Code is not written perfectly and git helps to identify where a bug may have a occurred so it can fixed by a coder. Especially if new piece of code reopens a new bug in software. In the next few parts, I will explain how to use git and later Github (which will be explained in a little bit here) to save your code locally and to the cloud. 

Now along with Git we have Github, which is the website where you can save your project to. These projects are saved into, what are called, repositories. These repositories are like project folders you save on Github. So for instance, if I have a coding project, and by extension folder, for a TODO application I would create a repository called "TODO app" on Github and I would be able to access this project on Github. But overall saving these projects on the cloud wit Github comes in handy as you are able to access the project from anywhere you want. Or least places with an internet connection :). Not only that it comes in handy when there are multiple people working on the same project. This allows for collaboration between a team developers and ease of auditing as each team member is able to see who has changed what. 

Below is like a simple workflow you would use with Git and Github to give you an idea of what its usage could look like: 

```bash
# Clone repository
git clone https://github.com/<your-username>/<repository-name>.git
cd <repository-name>

# Make changes
echo "Hello, World!" > hello.txt
git add hello.txt
git commit -m "Add hello.txt with a hello message"
git push origin main

# Collaborate
git checkout -b new-feature
echo "Another message" >> hello.txt
git add hello.txt
git commit -m "Add another message to hello.txt"
git push origin new-feature
```

Now don't be afraid about the commands that will be taught later. Just understand that these commands are used to interact with a repository using git and using git to push those changes to Github. 