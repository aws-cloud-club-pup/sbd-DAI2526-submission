# Submission Repository for SBD Department of AI Members

## What is this?
---
This repository will contain all the **submission of activities** by the members of DAI. Including but not limited to their *python projects*, *notebooks* and  *AI-powered applications.* 

This will serve as an installation and submission guide so that the members themselves can familiarize themselves with utilizing Git and GitHub.

#### Things to Note:
- You can only do `Pull Request (PR)` and the leads would be the one responsible for merging your request.
- Pushing to `main` branch is strictly ***not allowed.*** You are only allowed to submit in `submission` branch.
- If you have any questions or encountered some problems, please do not hesitate to contact the leads.

---
## Short Introduction to the Folders

The folders will be organized based on activity number and such. The repo will be updated every time a new activity is uploaded. 

Inside the folders on the dedicated activity number, there would be a `README` containing all the instructions needed to be done by the learner. 

---
# Set-Up Guide
## Installation (One-time Setup)

Install Git from [here](https://git-scm.com/install/) according to your operating system.
- To ensure you've installed Git properly, open your terminal and run 
 ```
	  git --version
 ```
- If it shows something like the output below, then you are in the right track.
```
	git version x.xx.x
```
	
- If you encounter an error, please verify your installation and ensure Git is added to your system's PATH environment variable. When the problem still persist, please contact the leads to help you with the setup.

From this point onwards, you'll be doing basic git commands only related to submission. If you wanna learn more about Git & GitHub, the workshop is in the LMS, alternatively, you can also refer to this [documentation made by GitHub](https://docs.github.com/en/get-started/git-basics/set-up-git).

---
# Submission Guide

Follow the following steps and only submit your work in `submissions` branch. This guide also contains on how you should name your file and commit messages. 

Again, please only submit your work in `submissions` branch. 

### 1. Prepare Your File(s)

The file format should be indicated in the activity instructions in the README, for this guide, let's assume that you are working with a Python Notebook and using Google Colab.

- **Filename format** should be: `SURNAME_Act[Number].ipynb` (e.g `LARDIZABAL_Act1.ipynb`)
- For multiple files, enclose them in a folder and the folder should follow the naming format from the prior instruction.

### 2. Download Your Notebook

Download your Colab notebook as an `.ipynb` file:
- Navigate towards the upper left then `File > Download > Download .ipynb`.
- Save the file with the correct filename format (`SURNAME_Act[Number].ipynb`)

### 3. Check Your Repository
- If you've already forked and cloned the repository from Step 4 and 5 (Forked and Cloned the repo)
	- Skip 4, 5, and 6. Jump to 7.
- If you haven't already forked and cloned the repository, follow the next few steps.

### 4. Fork the Repository (One-Time Setup)
- Go to the main repository page on GitHub.
- Click the `Fork` button in the upper right corner in between `Watch` and `Star`. This will allow you to create a copy of the repository under your GitHub account.
- This fork will allow you to make changes and submit pull requests.

### 5. Clone the Repository (One-Time Setup)

- Clone your forked repository into your computer using this git command:
```
git clone <forked-repo-url>
```
- Replace `<forked-repo-url>` with the URL of your forked repository. It can be found on GitHub under `Code`

- Navigate to the repository folder:
```
cd <repository-name>
```
- Alternatively, you can also navigate through the folder by pressing tab after typing `cd ` then pressing the Enter key.

### 6. Set Up the Upstream Remote (One-Time Setup)
- Add the original repository as an upstream remote to keep your repo updated on the changes done in the main repo.
```
git remote add upstream <original-repo-url>
```
- Replace `<original-repo-url>` with the URL of the main repository (`https://github.com/aws-cloud-club-pup/sbd-DAI2526-submission.git`)

### 7. Update your Local Repository (For Returning)
- If you already have the repository cloned, ensure your local copy is up-to-date with the main repository by running the following commands:
```
git fetch upstream
git checkout main
git merge upstream/main
```

- Push the updates to your fork:
```
git push origin main
```

### 8. Switch to the `submissions` branch
- Switch to the `submissions` branch in your local repository:
```
git checkout submissions
```
- If the `submissions` branch does not exist locally, pull it from the upstream repository:
```
git checkout -b submissions
git pull upstream submissions
```

### 9. Add Your Output to the Repository
- Put your file output into their respective activity number in your local repository
- Stage the file for commit:
```
git add <activityFolder_workshopname>/<SURNAME_act[number].ipynb
```

### 10. Commit Changes
- Commit your changes with a clear commit message.
```
git commit -m "SURNAME: Added my file submission for Activity (Number)"
```
- E.g `git commit -m "LARDIZABAL: Added my file submission for Activity 1`

### 11. Push Your Changes to `submissions` Branch
- Push your changes to the `submissions` branch in your forked repository
```
git push origin submissions
```

**P.S**: Branch protection rule is in order to prevent you from pushing in the `main` branch. If you did, you'll receive an error.

### 12. Create a Pull Request (PR)
- Go to your forked repository in GitHub
- You should see a big banner indicating that you recently pushed changes to the `submissions` branch
- Click `Compare & pull request`
- In the pull request:
	- Use the title: `Activty (Number) Submission - <Surname>` (E.g `Activity 1 Submission - Lardizabal`)
	- Add a description
	```
	Submission of Activity (Number) based on (Workshop Name): <FileName>
	```
	- If you worked with a group:
```
- Submission of Activity (Number) based on (Workshop Name): <FileName>
- In Collaboration with (Groupmate's Names)
```
- Ensure the PR is targeting the `main` branch of the original repo
- Submit the pull request.

---

## Troubleshooting Guide

- **Cannot push to `main` branch**: This is expected due to branch protection rules. Ensure you are pushing to the `submissions` branch.
- **Merge conflicts**: If your PR has conflicts, resolve them locally by pulling the latest changes from `upstream/main`, merging them into your `submissions` branch, and pushing the updated branch.
- **Need help with Git/GitHub**: Reach out to the project lead or refer to [GitHub's documentation](https://docs.github.com/en).

---
## Concerns

If you have any concerns, issues or in need of assistance. Please do not hesitate to contact your leads.

Let's all work together to uplift, learn, and move forward towards our tech journey! ❤️‍🔥🔥.
