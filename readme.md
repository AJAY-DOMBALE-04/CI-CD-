# CI/CD 

1) How to create the CI/CD pipeline in this repository i will learn, and  for that i am using my existing portfolio website which is made in single html page.

2) for this i am using GitHub Actions tool to run this CI integration process and which is inbuilt in the github so github action is easy to perform the CI(continous integration).

3) I will update all the steps in this file which i follow to create the CI/CD pipeline.

# what is CI(continous integration) ?

1) while developing any project what we do is  connect the project files to the github using the git and we have to create the repository on the github and connect the repository url using the git in the terminal of the project then we perform the git command and push the code to the github .

  # common command like 

   git init
   git add .
   git commit -m "first commit"
   git remote add origin "url"
   git branch -M main
   git push -u origin main

2) after we push the code to the github then we have to manually build our code before we deploy the code to the production means we cannot direct push the changes and the code to the live project.

3) after the build is success full then we can do the deployment and the code is deploy to the live  project but this whole process is manaully done and takes time and here we can make this process automate using the two process CI(continous integration which will build our code and check all the test case which we have set and if all the test case are pass by the code then only hte code sent ot the deployment if the test case fail then it shows error in the github which is easy for us to look specifically where the integration error has happen so no need manually build and check the test case ).

4)