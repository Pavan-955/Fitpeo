# Fitpeo
[1] Create Local Repo
----------------------
$ git init

[2] Stage Your Changes
------------------------
$ git add .              # Stage all files
$ git add <file>         # Or stage specific file(s)

[3] Commit Changes
------------------------
$ git commit -m "Meaningful commit message"

[4] Connect to Remote Repo
-----------------------------
$ git remote add origin <remote_repo_URL>

# Example:
$ git remote add origin https://github.com/yourname/repo.git

[5] Push to Remote Repo
-----------------------------
$ git push -u origin master      # First push
$ git push                       # Subsequent pushes

✅ Case 1: No Remote Repository Created Yet
🧩 Scenario:

You're working locally, but haven't created a remote repo (e.g., on GitHub/GitLab) yet.

📌 Steps:

Create a local repo

git init


Add files and commit

git add .
git commit -m "Initial commit"


Create a remote repo (on GitHub/GitLab/Bitbucket manually)

Add the remote repo to your local project

git remote add origin <REMOTE_REPO_URL>


Push your local code to the remote

git push -u origin master


Use main if your default branch is main.

✅ Case 2: Remote Repo Already Exists
🧩 Scenario:

The remote repo is already created and available, possibly by you or your team.

📌 Steps:
👉 If you're starting fresh locally:

Clone the remote repo

git clone <REMOTE_REPO_URL>
cd repo-name


Make changes, then add, commit, push

git add .
git commit -m "Your message"
git push

👉 If you already have local code (not cloned), but remote exists:

Initialize Git locally

git init


Add and commit your work

git add .
git commit -m "Initial commit"


Add the existing remote

git remote add origin <REMOTE_REPO_URL>


Push your code to the remote

git push -u origin master

⚠️ Common Errors to Watch Out For:

Pushing to a non-empty remote (e.g., README already exists remotely) may cause:

! [rejected] master -> master (fetch first)


Solution:

git pull origin master --allow-unrelated-histories
git push -u origin master
