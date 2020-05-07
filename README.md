Tools And Technologies Used

SCM System (git and GitHub)
Git Hooks For developer side Automation
Jenkins Build Automation
Containerization(Docker)
Docker Compose to build the environment
Bash Script
We have two server Testing Server and Production server 

We have to configure Jenkins in such a way that 

job 1st

It will monitor particular branch (ayush_dev) only and as soon as developer team pushes to that branch Jenkins job will be automatically triggered. Because i have configured webhook on github.



job 2nd

Then it will monitor master branch only and as soon as developer team pushes to master branch Jenkins job will automatically trigger. This only runs after succesful run of Job 3rd since that is configured to push code to master branch .Let's see Job 3rd below.



Job 3rd

We pretend to be QA Team and we run a script to test server if everything is fine

if fine then it triggers the Job 3rd

Jenkins Job 3rd is configured to be triggered remotely from Testing Team.

Once it is triggered it merges the master branch and ayush_dev branch and then trigger Job 2nd.

We can see the complete flow is automated only the Testing Team have to run a script.

I have uploaded a presentation video on linkedin article which will help to understand better.
Video_Link: https://www.linkedin.com/pulse/lwdevops-task-project-ayush-kumawat/?published=t
