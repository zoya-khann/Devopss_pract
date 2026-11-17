# STEP 1: Create a project directory
mkdir GitPractical
cd GitPractical

# STEP 2: Initialize a Git repository
git init

# STEP 3: Configure Git username and email
git config --global user.name "Your Name"
git config --global user.email "yourmail@gmail.com"

# STEP 4: Create an HTML file
notepad index.html

# Add the following HTML code inside index.html:
# <html>
# <body>
# <h1>Welcome to Git</h1>
# </body>
# </html>

# STEP 5: Add the file to the staging area
git add index.html

# STEP 6: Commit the changes
git commit -m "First commit"

# STEP 7: Check repository status
git status

# STEP 8: View commit history
git log --oneline


# STEP 9: Create a repository on GitHub
# Log in to GitHub and create a repository named GitPractical.

# STEP 10: Connect the local repository to GitHub
git remote add origin https://github.com/username/GitPractical.git

# STEP 11: Rename the current branch to main
git branch -M main

# STEP 12: Push local code to GitHub
git push -u origin main


# STEP 13: Clone the GitHub repository
# Move outside the original project directory
cd ..

# Download a copy of the remote repository
git clone https://github.com/username/GitPractical.git GitPractical-copy

# STEP 14: Return to the original project directory
cd GitPractical

# STEP 15: Pull the latest changes from GitHub
git pull origin main

# If the local and remote repositories have unrelated histories,
# use this command for the initial pull instead:
# git pull origin main --allow-unrelated-histories

# STEP 16: Fetch remote changes without merging
git fetch origin


# STEP 17: Check available branches
git branch

# STEP 18: Create and switch to a new feature branch
git checkout -b feature

# STEP 19: Open index.html and change the heading
notepad index.html

# Change the heading to:
# <h1>Welcome to Feature Branch</h1>

# STEP 20: Stage and commit feature branch changes
git add index.html
git commit -m "Updated feature branch"


# STEP 21: Switch back to the main branch
git checkout main

# STEP 22: Open index.html again
notepad index.html

# Change the same heading to:
# <h1>Welcome to Main Branch</h1>

# STEP 23: Stage and commit main branch changes
git add index.html
git commit -m "Updated main branch"


# STEP 24: Merge feature branch into main branch
git merge feature

# A merge conflict will occur because both branches
# modified the same line in index.html.

# STEP 25: Open the file to resolve the conflict
notepad index.html

# Remove conflict markers and keep both headings.
# Final index.html content:

# <html>
# <body>
# <h1>Welcome to Main Branch</h1>
# <h1>Welcome to Feature Branch</h1>
# <p>Updated from GitHub</p>
# </body>
# </html>

# STEP 26: Add the resolved file
git add index.html

# STEP 27: Commit the resolved changes
git commit -m "Resolved merge conflict"


# STEP 28: Push merged changes to GitHub
git push origin main

# STEP 29: Check repository status
git status

# STEP 30: View all commits
git log --oneline

# STEP 31: Check available branches
git branch

# STEP 32: Check connected remote repository
git remote -v
