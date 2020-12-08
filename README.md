# murder
A collaborative group game to practice using git.

## Scenario ## 
A murderer is on the loose! 

Victims can be seen on the [live site](https://lucitemple.github.io/murder/). If your name turns red, you have been poisoned. To save yourself use git and GitHub to cure yourself with the antidote.

## Set Up for Players ##
1. Give the game master your GitHub user name so they can add you as a repo collaborator. 
2. Open the Terminal/Command Line and navigate to the local folder you want to work in.
3. Clone the repository to your local machine: `git clone https://github.com/lucitemple/murder.git `
4. Navigate into the local repository: `cd murder`

## How To Play ##
1. Open the [live site](https://lucitemple.github.io/murder/) in a web browser to see who has been poisoned.
2. If your name turns red:
   - Cure yourself before the game ends (when time runs out)!
   - _If you need help, you can screen share on Zoom and take advice from other players._
   - In the Terminal:
     - Pull the most recent code from GitHub: `git pull`
     - Create a new branch and switch to it: `git branch -b <newbranchname>`
     - Open the html file in your code editor: `code index.html`
   - In the html file:
     - Find the card with your name. There will be a class on the card called "poison". Change "poison" to `antidote`.
     - Pick another card, with another person's name. Add the `poison` class to their card.
   - In the terminal: 
     - Add the file to staging area: `git add index.html`
     - Commit changes, with message: `git commit -m "Cure` `<yourname>` `: Poison` `<victimname>"`
     - Push changes to the remote repository: `git push -u origin <branchname>`
   - Open the [GitHub repository](https://github.com/lucitemple/murder) in your web browser.
   - Open a "pull request" to merge your branch with main.
3. If someone else's name turns red, and they need help, give them support.

Optional Round 2:
_Once everyone has been poisoned and cured once, introduce "`poison2`" and "`antidote2`" for another round._
1. If the background of your card turns pink:
   - In the Terminal:
     - Checkout the main branch: `git checkout main`
     - Pull the most recent code from GitHub: `git pull main`
     - Checkout your existing branch: `git checkout <branchname>`
     - Merge to update your branch: `git merge main`
     - Open the html file in your code editor: `code index.html`
   - In the html file:
     - Find the card with your name. There will be a class on the card called "poison2". Change "poison2" to `antidote2`.
     - Pick another card, with another person's name. Add the `poison2` class to their card.
   - In the terminal: 
     - Add file to staging area: `git add index.html`
     - Commit changes with message: `git commit -m "Cure` `<yourname>` `: Poison` `<victimname>"`
     - Push changes to the remote repository: `git push -u origin <branchname>`
   - Open the [GitHub repository](https://github.com/lucitemple/murder) in your web browser.
   - Open a "pull request" to merge your branch with main.
2. If someone else's card turns pink, and they need help, give them support.


## Set Up for Game Masters ##
1. Fork this repo to your own
2. Host it on GitHub Pages
3. Edit the README.md file to update the repository info and live site link to your own.
4. Edit the index.html file to add the names of your players to the cards.
5. Add the players as collaborators to your fork's GitHub repository. (Settings > Manage Access > Invite collaborators)
6. Create a branch protection rule on 'main'. (Settings > Branches > Branch protection rules > Add rule > `main` > Require pull request reviews before merging)
7. Gather players to play, ideally in a way they can support one another if they are not confident in using git. E.g. a Zoom session where they can screen share.

## In-game responsibilities for Game Masters ##
1. Explain the rules, make sure everyone is set up to play, set a timer for however long you want to play.
2. Facilitate screen sharing, and support any struggling players if other players are not forthcoming. _This is a learning exercise, aimed at helping newbies gain pracice and confidence in these git commands (not a competitive game!)._
3. Review pull requests to the repo as they are made, ensuring they match the requirements:
   - Commit message is in the correct format "Cure `<playername>` : Poison `<victimname>`"
   - The antidote and poison classes have been applied correctly for the game to proceed.
3. Call time when the timer is up. Announce the dearly departed (whoever is currently in a poisoned state). Congratulate everyone on their efforts & check to see if people now feel more confident using Git.

