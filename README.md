# murder
A collaborative group game for practicing git.

## Scenario ## 
A murderer is on the loose! To save yourself after being poisoned, use git and GitHub, to cure yourself with the antidote.

## Set Up for Players ##
1. Join your group on Zoom to play, taking turns to screenshare and helping each other out.
2. Ensure all team members are collaborators on the repo. Everyone will have accepted the email invitation.
3. Open the Terminal/Command Line and navigate to the local folder you want to work in.
4. Clone the repository to your local machine
5. Navigate into the local repository: `cd murder`

## How To Play ##
1. Open the live site in a web browser to see who has been poisoned. 
   - Note: GitHub Pages takes time to load changes in browser. It is faster to look at recent commits in the repo if you are comfortable doing so.
2. If your card is poisoned:
   - Cure yourself before the game ends (when time runs out)!
   - _If you need help, ask other players._
   - In the Terminal:
     - Pull the most recent code from GitHub: `git pull`
     - Create a new branch: `git branch <newbranchname>`
     - Switch to new branch: `git checkout <newbranchname>`
     - Open the html file in your code editor: `code index.html`
   - In the html file:
     - Find the card with your name. On the card, there will be a class in the h5 tag called "poison". Add `antidote`to the h5 class.
     - Pick another card, with another person's name. Add the `poison` class to the h5 tag on their card.
   - In the terminal: 
     - Add the file to staging area: `git add index.html`
     - Commit changes, with message: `git commit -m "Cure` `<yourname>` `: Poison` `<victimname>"`
     - Push changes to the remote repository: `git push -u origin <branchname>`
   - Open the GitHub repository in your web browser.
   - Open a "pull request" to merge your branch with main.
   - Assign the pull request to a reviewer.
3. If you are assigned to review a pull request: 
  - review the pull request
  - approve it
  - merge the new branch into main
  - close the pull request
  - delete the extra branch after it was merged
4. If someone else's name turns red, and they need help, give them support.

## GitHub Cheatsheet

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

### Clone the repository

- [Documentation](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository)
- Copy the GitHub repository address
- In VSCode open a terminal/command line
- Navigate to the directory in which you wish to keep the repository. e.g. Documents or Projects.
- Use the below command with your own repo address

  `git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY`

### Create and checkout branch

- [Detailed instruction](https://www.atlassian.com/git/tutorials/using-branches)
- Navigate into the local repo using the command `cd`
- Create a branch in your name using the below command.

  `git branch your-branch-name`

- Checkout the branch to work on it

  `checkout your-branch-name`

### Make changes and save to GitHub repo

- Make changes to your file.
- Add changes to the staging area

  `git add .`

- Commit changes

  `git commit -m "Cured my-name. Poisoned victim-name`

- Check status

  `git status`

- Push branch to GitHub

  `git push --set-upstream origin your-branch-name`

### Create Pull Request

- [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)
- On the GitHub repo page, click on the 'Compare & pull request' button.
- Add a comment to the pull request explaining the additions to your branch. "Cured my-name. Poisoned victim-name".
- Add a teammate as a “reviewer”. [Here's how](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review).

### Review and Merge Pull Request

- [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/reviewing-changes-in-pull-requests/reviewing-proposed-changes-in-a-pull-request)
- On GitHub, navigate to the open pull request
- You may need to click on "files changed" to see the changes. Compare the code in the new branch to the main branch, to see what has been changed and avoid code conflicts.
- Click on the "review changes" button
- Either "approve" or "request changes", and "submit review".
- After the pull request has been approved, press the button to "merge" the new branch into the main branch. [Documentation](https://docs.github.com/en/github/collaborating-with-pull-requests/incorporating-changes-from-a-pull-request/merging-a-pull-request)
- ‘Close’ the pull request (button)
- Delete the merged branch (your-name-branch) on GitHub

### Fetch and Pull

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

### Extra things to try

#### Delete local branch

After you have deleted a branch on GitHub, you will want to delete it from your local repository.

- [Documentation](https://www.freecodecamp.org/news/how-to-delete-a-git-branch-both-locally-and-remotely/)
- In VSCode terminal/command line, checkout the main branch

  `git checkout main`

- Delete the local feature branch

  `git branch -d your-branch-name`

#### Local merge

If you have already been working on your own branch, and want to bring new updated code from the main branch into your existing branch:

- [Documentation](https://www.atlassian.com/git/tutorials/using-branches/git-merge)

- In VSCode terminal/command line, checkout your new branch

  `git checkout your-branch-name`

- Merge the main branch into your new branch

  `git merge main`

#### Main branch protection

Protect the main branch from being accidentally overwritten or corrupted by forcing a review process on GitHub.

- [Documentation](https://docs.github.com/en/github/administering-a-repository/defining-the-mergeability-of-pull-requests/managing-a-branch-protection-rule#creating-a-branch-protection-rule) 
- On GitHub, on your repo page:
- Settings > Branches > Branch protection rules > Add rule > 'main' > Require pull request reviews before merging


#### Add collaborators

Add team members to the repository as ‘Collaborators’.

- [Here's how](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository)
- On your GitHub repo page:
- Settings > Manage Access > Invite collaborators
- You will need to know your teammate’s GitHub username or email address
- Team members must accept the ‘invitation’ to be collaborators. Check your emails, including spam folder, for the invitation.

#### Configure GitHub Pages

- [Here's how](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)
