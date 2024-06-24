


#### Top tips

##### Navigating GitHub

![image](https://github.com/ncpeters/DEMO/assets/131660276/3337e9c8-f42e-4904-a030-bab4d0c6cb39)

1. Username: GitHub user’s name (account).
2. Repository: project directory (also known as repo). In this example, the repository name is “trial-repo”.
3. Code: this tab brings you back to your landing page. It shows you the folders that you have made in the repo.
4. Main: this is your default development branch or active branch of your repository.
5. Branch: parallel version(s) of your repository.
6. README.md file: this file contains basic information about your project (in this case it only has the project name: “trial-repo”. When we plan to make a website, this will be rendered as a landing (front) page for your site.
On the right side of the webpage we have the following features:
7. Green Code button: click it to download your repository locally.
8. ‘+’ symbol: where you can create new repository, import repos and create new issues.
9. Fork: create a personal copy of another user’s repo. The number shows how many forks there are of your current repository.
10: Add file: create or upload a file to your repository.
11: Commits/clock symbol: click to see the history of this file as a list of all the edits (commits) saved at different time points.
12: Edit/Pencil symbol: click this pencil symbol to edit your README.md file.

Adapted from First steps on GitHub — The Turing Way (the-turing-way.netlify.app) 


##### Branches

- Develop new features on their own branches, which you can create via _git checkout -b branch_name_ and switch between via _git checkout branch_name_.
- Make sure each branch has a single purpose and only changes related to that purpose are made on it.
- Make sure branches have informative names.
- Make sure the main branch is kept clean.
- Delete a branch once that portion of work is complete.

##### Commits

- Commit and push often - do not assume that because it is saved locally it is safe.
- Each commit should make one simple change.
- No generated files committed.
- Commit messages are meaningful, with a ~50 character summary at the top.
- Commit messages are in the present tense and imperative.


![image](https://github.com/ncpeters/DEMO/assets/131660276/5fc97f97-b904-4f47-acc0-ed11678683a0)


##### Merging

- Always assign a reviewer (other than yourself) to a pull request for merging
- Merge other’s changes into your work frequently by running _git pull_
- You need to _git pull_ on main and on branches when updating your local repository - _git pull_ on one branch will not update the others
- When dealing with merge conflicts, make sure you fully understand both versions before trying to resolve them.


##### Git commands


###### The mysterious inner workings of _git add_ and  _git commit_

![image](https://github.com/ncpeters/DEMO/assets/131660276/730a81f8-755d-475a-a8fd-3c5d430c61bf)

(https://the-turing-way.netlify.app/reproducible-research/vcs/vcs-git.html)

###### How do SVN and Git compare when it comes to their commands and terms?

Beware: Subversion (SVN) and Git share similar vocabularies – the commonality often is only the command names; behaviour and functionality are quite distinct.

See the below table for a (non-exhaustive) comparison of terms and functionality: 

![image](https://github.com/ncpeters/DEMO/assets/131660276/a9a663af-0de9-4b06-8678-bce0fbcd4814)




