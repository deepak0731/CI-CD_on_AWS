# DevOps_on_AWS(CI-CD)
 Demonstration of continuous integration/ continuous delivery with the help of AWS resources  like Codecommit, CodeBuild, CodeDeploy and CodePipeline.
## Set Up GitHub Repository
The first step in our CI journey is to set up a GitHub repository to store our source code. If you already have a repository, feel free to skip this step. Otherwise, let's create a new repository on GitHub by following these steps:
- Go to github.com and sign in to your account.
- Click on the "+" button in the top-right corner and select "New repository."
- Give your repository a name and an optional description.
- Choose the appropriate visibility option based on your needs.
- Initialize the repository with a README file.
- Click on the "Create repository" button to create your new GitHub repository.

Great! Now that we have our repository set up, we can move on to the next step.


## Create an AWS CodeRepository

In this step, we'll create an AWS CodeRepository,  Let's go ahead and set it up:
- Navigate AWS console and serch for AWS CodeCommit,
- Select repository and create one.
- Give name to a repository, and disription accordingly.
- leave everything as default.

 
## Create IAM User for respective operation

In this step, we'll create IAm user.
- Navigate AWS console and search IAM.
- Go to Add user
- Provide username along with access of console
- Give AWSCommitPowerUser permission to the user so that we can perform our task ( you can also give FullAdministrativePermission for more easier but only for tutourial purpose)
- create HTTPS Git credential For AWS COdeCommit for the same user
- Save the credentials for safer side


## Now go on CodeCommit and clone the repository with CLone URL
- Go to copy URL
# open the local Terminal or VS_Code

- enter the git clone < URL >
- now put your HTTPS Git credential For AWS COdeCommit in popup window
- create a file here and write a basic code of Index.html for demo purpose
- now run the command =>
- git add .
- git commit -m "msg"
- git push origin master
So, by doing this you can connect your local with AWS master by using AWS CodeCommit.
- Lets create a branch here,
- git checkout -b Branch_Name
- now you can merge branches by creating a pull request from new branch
- you can also provide Approval Rule Template in which you can fix the number of approval required merge.

## CodeBuild (works like Jenkins)

- Navigate the console and go to the CodeBuild
- create a Build Project
- set a project name
- add a discription ( optional )
- navigate source eg- github, S3, codecommit
- choose a repository which we make earlier
- select master branch
- in the Environment
- selct managed image with Linux/Ubuntu
- create and select a service role for codebuild service
- now for buildspec you can create buildspec file or select mine file ( buildspec.yml ) as well
- create build project by select build
- your build is created
- save this in by choose edit/Artifacts
- select S3/create bucket
- fill info and
- Update Artifact.
- 
