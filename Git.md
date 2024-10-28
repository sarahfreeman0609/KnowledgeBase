# Git

### SSH key set up
1. Generate ssh key
````
ssh-keygen -t ed25519 -C "sahar.aghayeva@gmail.com
````
It will generate the pair of private `/home/sahar/.ssh/id_ed25519` and public `/home/sahar/.ssh/id_ed25519.pub`keys 
2. Copy contents of public key `/home/sahar/.ssh/id_ed25519.pub` and create SSH key based on that on your github settings https://github.com/settings/keys

### Tagging
````
git tag -a 0.0.1 COMMIT_HASH
git show 0.0.1
git push origin 0.0.1
````

### Show origin
````
git remote show origin
````

### List ignored files
````
git ls-files . --ignored --exclude-standard --others
````

### List untracked files
````
git ld-files . --exclude-standard --others
````

### Squash multiple commits
Here in example we're squashing the last 3 commits together
````
git rebase -i HEAD~3
````

### Add ready local project to the existing empty remote repo
1. In the local project folder run
````
git init
````
2. Add remote origin
````
git remote add origin git@gitlab.com:TEST_USER/TEST_LINK_TO_REPO.git
````
3. Add all files and push to remote
````
git add .
git commit -m "Initial commit"
git push -u origin main (or master)
````

### Rename existing branch
````
git checkout OLD_BRANCH_NAME
git branch -m NEW_BRANCH_NAME
````

### Git command generation tool
https://www.gitmecmd.xyz/