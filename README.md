# dexp1
Perform Git operations to commit, push, merge branches, and create a pull request on GitHub.
Git
GitHub
Step 1 – Initialise repo & first commit
bash
copy
# Initialise a local repository
git init myproject
cd myproject

# Create a file and make the first commit
echo "# My DevOps Project" > README.md
git add README.md
git commit -m "Initial commit: add README"
Step 2 – Create a feature branch & make changes
bash
copy
git checkout -b feature/hello

echo "Hello from feature branch" > hello.txt
git add hello.txt
git commit -m "feat: add hello.txt"
Step 3 – Push to GitHub & open Pull Request
bash
copy
# Connect to remote (first time only)
git remote add origin https://github.com/<username>/myproject.git
git push -u origin feature/hello
ℹ️
On GitHub → go to your repo → click Compare & pull request → add a description → click Create pull request.
Step 4 – Merge & push main
bash
copy
git checkout main
git merge feature/hello
git push origin main
git log --oneline --graph
