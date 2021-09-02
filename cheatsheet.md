# GitHub Cheatsheet
- [Clone the repository](#clone-the-repository)
- [Create and checkout branch](#create-and-checkout-branch)
- [Make changes and save to GitHub repo](#make-changes-and-save-to-github-repo)
- [Create Pull Request](#create-pull-request)
- [Review and Merge Pull Request](#review-and-merge-pull-request)
- [Fetch and Pull](#fetch-and-pull)
- [Delete local branch](#delete-local-branch)
- [Local merge](#local-merge)
- [Main branch protection](#main-branch-protection)
- [Add collaborators](#add-collaborators)
- [Configure GitHub Pages](#configure-github-pages)

## Clone the repository 
- [Documentation](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository)
- Copy the GitHub repository address
- In VSCode open a terminal/command line
- Navigate to the directory in which you wish to keep the repository. e.g. Documents or Projects.
- Use the below command with your own repo address

    `git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY`

## Create and checkout branch 
- [Detailed instruction](https://www.atlassian.com/git/tutorials/using-branches)
- Navigate into the local repo using the command  `cd` 
- Create a branch in your name using the below command.

    `git branch your-branch-name`

- Checkout the branch to work on it 

    `checkout your-branch-name`

## Make changes and save to GitHub repo
- Make changes to your file.
- Add changes to the staging area

    `git add .`

- Commit changes

    `git commit -m "Cured my-name. Poisoned victim-name`
- Check status

    `git status`
- Push branch to GitHub 

    `git push --set-upstream origin your-branch-name`

## Create Pull Request
- [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- On the GitHub repo page, click on the 'Compare & pull request' button.
- Add a comment to the pull request explaining the additions to your branch. "Cured my-name. Poisoned victim-name". 
- Add a teammate as a “reviewer”. [Here's how](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).

## Review and Merge Pull Request
- [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request)
- Navigate to the open pull request
- You may need to click on "files changed" to see the changes. Compare the code in the new branch to the main branch, to see what has been changed and avoid code conflicts.
- Click on the "review changes" button
- Either "approve" or "request changes", and "submit review".
- After the pull request has been approved, press the button to "merge" the new branch into the main branch. [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)
- ‘Close’ the pull request (button)
- Delete the merged branch (your-name-branch) on GitHub

## Fetch and Pull
- In your terminal/command line, in the repo directory
- Checkout the main branch  

    `git checkout main`
- Fetch information about the newest code on github to your local repo

    `git fetch`
- Compare the code on your local repo to the remote repo

    `git status`
- Pull new code down.

    `git pull`
- [Create & checkout new branch](#create-and-checkout-branch)

## Extra things to try

### Delete local branch
After you have deleted a branch on GitHub, you will want to delete it from your local repository.
- [Documentation](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/)
- Checkout the main branch

    `git checkout main`

- Delete the local feature branch

    `git branch -d your-branch-name`

### Local merge
If you have already been working on your own branch, and want to bring new updated code from the main branch into your existing branch:
- [Documentation](https://www.atlassian.com/git/tutorials/using-branches/git-merge)

- Checkout your new branch

    `git checkout your-branch-name`
- Merge the main branch into your new branch 

    `git merge main`  

### Main branch protection 
Protect the main branch from being accidentally overwritten or corrupted by forcing a review process. 
- [Documentation](https://docs.github.com/en/github/administering-a-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule#creating-a-branch-protection-rule)
- In the GitHub repository Settings, go to Branches, and create a branch protection rule on the ‘main’ branch.
- Select the option “Require pull request reviews before merging”

### Add collaborators
Add team members to the repository as ‘Collaborators’. 
- [Here's how](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)
- You will need to know your teammate’s GitHub username or email address
- Team members must accept the ‘invitation’ to be collaborators. Check your emails, including spam folder, for the invitation. 

### Configure GitHub Pages
- [Here's how](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)

