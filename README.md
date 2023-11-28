# My-project

Assignment: use GitHub Actions to implement a continuous deployment pipeline. 

The continous deployment pipeline should look like this:
1. You manually write, commit and push some code. This only requires you to be familiar with git.
2. GitHub Actions runs tests on your code. You can use Pytest for this.
3. If and only if the tests pass, GitHub Actions logs into the VPS you have running with Digital Ocean and runs commands such that the code is updated to the latest version.

The only new part here is step 3, and we will let you think about how to best implement this. 

Tips: 
- Github deploy keys
- sh files
- secrets


  Step 1:
  Create repository on Github
  from previous assignments 'my-project' and 'farm'

  Step 2:
  CREATE A GITHUB ACTIONS WORKFLOW FILE TO HANDLE YOU CI/CD PIPELINE TO DIGITAL OCEAN
  This was done with a yml file in previous assignment

  Step 3:
  CREATING A SERVER ON DIGITAL OCEAN AND GENERATING SSH KEYS
  Droplet already made in assignment. generated SSH keys

  Step 4:
  ADDING SECRETS IN YOUR REPOSITORY THAT WILL ENABLE SSH KEYS

  Step 5:
  CONFIGURING OUR DEPLOY.YAML FILE TO EXECUTE AFTER A COMMIT AND PUSH TO MAIN
  
  
  
