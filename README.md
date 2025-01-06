# NYC Data Science January 6 Cohort


This repository contains all lectures for the January 6th 2025 Data Science Cohort.

### Setting up your lecture repo

In order to connect to this repo, you will:

1. Fork this repository.
2. Clone your fork of this repository.
3. By the end of the previous step, you should have a pointer to the remote repository you just forked. The remote name should be called origin and will point to your forked repo.

When you type: git remote -v

You should see something like this:

origin  https://github.com/your_user_name/NYC_DS_010625.git (fetch)

origin  https://github.com/your_user_name/NYC_DS_010625.git (push)

If not, type: git remote add origin main <forked_git_repo_address>

4. As it stands your local repository only points to one remote repository: your fork (origin).

When lectures are added, you will need to be able to get updates from the main lecture repository (i.e. what is on admveen) and update your fork and local repository. We thus need to add another remote repository which will point to the location where the instructional team will add lectures. It is customary to denote the alias to this original repository as **upstream**.

git remote add upstream git@github.com:admveen/NYC_DS_010625.git

If you have done this correctly, then you will see the following upon enter "git remote -v" in your terminal


origin  https://github.com/your_user_name/NYC_DS_010625.git (fetch)

origin  https://github.com/your_user_name/NYC_DS_010625.git (push)

upstream  https://github.com/admveen/NYC_DS_010625.git (fetch)

upstream  https://github.com/admveen/NYC_DS_010625.git (push)

### Getting new lectures (updates from the upstream)

When you are ready to get updates from the main lecture repo, type:

git fetch upstream 

This will fetch a commit history of all branches on the main lecture repository. You can inspect changes and compare them to your local and forked repository before deciding to merge commits on the main lecture repository with your local main branch.

When you are ready to get the new updates, make sure that you are on your local repo's main branch. Then type:

git merge upstream/main

If you keep your main branch on your repository as close as possible to the original lecture repository's main branch, then you should not get merge conflicts and will see updates in your local repo.

**Words of advice:** If you are going to make a lot of changes to the lecture notebooks as you go, it might be a good idea to checkout a different branch and commit your changes there in that branch. Whenever a new lecture becomes available and you have pulled from upstream/main to your local main make sure that you then checkout your branch and merge the changes from main. This ensures that your modifications are made only in the branch, and the local repo's main branch as close as possible to the upstream's main branch.

Finally, make sure to do a "git pull origin main" then "git push origin main" on your local repo's main branch. This will push what you have pulled from upstream/main to your forked remote repo (i.e. your origin/main).


You may get merge conflicts when merging main into your branch. VS Code is a good option to resolves these conflicts and you can decide whether you will keep the changes you have made to the notebook vs. changes I may have made.

Finally, if maintaining a branch is too much of a pain: an easy thing to do is just to keep a separate folder (elsewhere on your hard drive and not a repository) where you copy contents of the lecture notes you pull from upstream. You can edit the notebooks in this folder without fear of messing up your ability to pull the lectures. 

### Accessing the lectures and optimizing your viewing experience

With the exception of the first two days of lectures, all lectures are in Jupyter notebook format and are meant to be viewed via the Jupyter RISE extension. In order to install this:

https://rise.readthedocs.io/en/stable/installation.html

I would recommend the conda installation.

Many of the lectures also split cells into columns for side by side viewing of text descriptions on one side and a code cell on the other. To view these, you'll need Jupyter notebook extensions:

In bash conda install the following:

conda install -c conda-forge jupyter_contrib_nbextensions
conda install -c conda-forge jupyter_nbextensions_configurator

- Then restart jupyter notebook and you will see a NBExtension tab. 
- Enable Split Cells Notebook.

If you get stuck: https://www.youtube.com/watch?v=Pls9sOQ2x_s
