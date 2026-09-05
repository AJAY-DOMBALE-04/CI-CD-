# CI/CD

## 1. Project Objective

In this project, I am learning how to create and implement a CI/CD pipeline using my existing portfolio website.

My portfolio is a static website created using a single HTML file containing the website's HTML, CSS, and JavaScript.

I created a separate GitHub repository for learning CI/CD so that I can understand the complete process without involving my existing Vercel deployment.


## 2. Tool Used

For implementing CI/CD, I am using **GitHub Actions**.

GitHub Actions is a GitHub feature that allows us to automate workflows whenever specific events happen in our repository, such as pushing code or creating a pull request.

I will use GitHub Actions to implement both:

* CI — Continuous Integration
* CD — Continuous Deployment


# What is CI (Continuous Integration)?

Continuous Integration is a development practice where changes made to a project are automatically checked and validated when they are integrated into the shared code repository.

In a typical development workflow, we connect our local project to a GitHub repository using Git.

Some common Git commands are:


git init

git add .

git commit -m "first commit"

git remote add origin "repository-url"

git branch -M main

git push -u origin main


After pushing our code to GitHub, we can use GitHub Actions to automatically perform checks on the code.

For example:


Developer makes changes
        ↓
      git push
        ↓
GitHub repository
        ↓
GitHub Actions starts
        ↓
Run automated checks
        ↓
     ┌───────┴───────┐
     ↓               ↓
   PASS             FAIL
     ↓               ↓
Continue          Show error
to next step      in GitHub


The purpose of CI is to detect problems automatically instead of depending completely on manual checking.



# What is CD (Continuous Deployment)?

After the CI checks are completed successfully, we can automate the deployment of the application.

This is where Continuous Deployment comes into the process.

The overall flow becomes:


Code Change
     ↓
   Git Push
     ↓
GitHub Repository
     ↓
GitHub Actions
     ↓
      CI
     ↓
Automated Checks
     ↓
   ✅ Passed
     ↓
      CD
     ↓
Automatic Deployment
     ↓
Live Website

If the CI checks fail:

Code Change
     ↓
   Git Push
     ↓
GitHub Actions
     ↓
CI Checks
     ↓
   ❌ Failed
     ↓
Deployment is not performed


This helps prevent a change that has failed the required checks from being deployed.



# GitHub Actions

GitHub Actions is the automation tool I am using to implement the CI/CD process.

The workflow configuration will be stored inside:


.github/
└── workflows/


The workflow file will define:

* When the workflow should run
* What environment should be used
* What checks should be performed
* What happens when the checks succeed
* What happens when the checks fail
* How the deployment is performed



# My CI/CD Implementation

I will document the implementation step-by-step below as I build the pipeline.

### Step 1 — Create the repository

Created a separate GitHub repository for learning CI/CD.

### Step 2 — Add the portfolio

Added my existing static HTML portfolio to the repository.

### Step 3 — Configure GitHub Actions

Created a GitHub Actions workflow to automatically perform CI checks.

### Step 4 — Test CI

I will make changes to the portfolio and push them to GitHub to verify that the CI workflow runs automatically.

I will also intentionally introduce an error to understand how a failed CI workflow behaves.

### Step 5 — Configure CD

After understanding CI, I will configure automatic deployment.

### Step 6 — Test the complete CI/CD pipeline

The final workflow will be:

Change portfolio
       ↓
    git push
       ↓
GitHub Actions
       ↓
      CI
       ↓
Automated checks
       ↓
    ✅ Passed
       ↓
      CD
       ↓
Automatic deployment
       ↓
Live portfolio

I will document each step, configuration, error, and solution in this README.
