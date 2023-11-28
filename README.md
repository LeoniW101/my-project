# Report CD assignment

For the final assignment of my Full Stack development course the goal was: use GitHub Actions to implement a Continuous Deployment pipeline to Digital Ocean Droplet. 

Meaning when you have written or changed code and you commit and push it, Github actions will run tests on your code (with Pytest). 
Only when these tests pass, Github actions will log into the VPS ( the droplet on Digital Ocean) to run the commands to update the changed/new code. 

During the course I already had to set up a droplet on Digital ocean, and get a flask app connected to that using WSGI and Gunicorn. This was already quite a challenge for me, but with some help it worked out. 
There was also another assignment in the course to get familiar with github actions and testing. 
That means for the most part for the final assignment I was well on my way having the basics set up from the course. 

Because I didn’t feel like I really understood the assignment I googled about the assignment. It turns out there are quite some helpful blog posts and video’s out there on this topic. 

Although I was really dreading this last assignment, I decided to just get started with the help of one of these blogs where all the steps were explained. Below an overview of these steps that also name several components and what problems I ran into as well as how these were fixed.  

## Step 1:  Create repository on Github. 
I had already done so from the course, so this was an easy step. 


## Step 2: Create a github actions workflow file to handle CI/CD pipeline to digital ocean.  
Although I learned from the course I had to use a .yml file for this, and had some general understanding about this I wasn’t sure what this exactly had to look like.   

## Step 3:   Creating a server on digital ocean and generating SSH keys 
The Droplet on Digital Ocean was already made during the course. But the SSH keys were completely new to me to work with. I followed the steps from the blog and managed to generate them. 
From Slack I learned that the public key can be seen as the lock, and the private key can be seen as the key to that lock. Which makes sense if you think about it!

##  Step 4: Adding Secrets to your Github Repository that will enable SSH Keys 
The explanation of how to add SSH keys to a Github repository were fairly simple, however, making sure they are copied and pasted correctly and in the right places was a challenge to understand. Eventually it worked out with some extra clarifications, and someone else noticing the only mistake there was: in the GitHub action I was referring to ‘SSH_PRIVATE_KEY’ and the actual name of the key was simply ‘SSH_KEY’.
Sometimes the solution can be so simple!

##  Step 5: Configuring our deploy.yml file to execute after a commit and push to main
This was a tricky one as in on the blog they were deploying a nodeJS and not flask. Since I wanted to have some more reference material I looked up some material from other repositories, and studied them for a few hours to get a sense of what mine should look like to work. 
It took some fiddling around, and with some guidance from a mentor I managed to understand what I was doing in the deploy.yml and on the server side. 
I had to change my flask app from the original location to the new repository local folder, and also amend on the server from Root to home. As root is normally used for administrator roles, and home for general users it made sense to put it in there. 

##  Step 6: Confirming our action has executed and viewing the action logs
### and
##   Step 7:   Check out deployed repository on the server
Although I had been looking into the action logs a lot already, this time it was very satisfying to see everything was oke there. And especially seeing my changes to the code being updated automatically on the server! 

### Conclusion
Even though I was dreading this final assignment thinking it would take me several weeks to complete, it turned out to be easier than I assumed. But, I think in the future I will prefer to leave this up to the real back end experts.
  
  
  
