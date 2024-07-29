# Pulling and Pushing

##  What Is It and Why Use It?

There two main commands when it comes to Github in terms of uploading and downloading your repository are ```git push``` and ```git pull``` respectively. If you are working with a team it is important to understand differences in changes to the code from what you made what was made in the main branch. ```Note: A branch is like a copy of the main code base you can use and eventually merge back into the main code base.```. The reason for needing to know these differences is to make sure you do not overwrite what the main code has. If you do overwrite the main branch it could break what the main code base is supposed to do, causing major issues. Additionally, these branches help to keep the local copy for a developer to manipulate, change, and test for themselves. But a single person or with a few people this should be a major issue to content with, but it is something to keep in mind when you are in a team.  

But continuing, the commands to git pull and push after committing is below:

```bash
git pull origin main
git push origin main
```

In the case you dealing with a different branch you would change ```main``` to your branch title

But more or less that's really it. Other than figuring out why your branch won't merge into main (which will probably take like 1-2hrs :\) ), your good to go with your basic git knowledge for a single to few devs