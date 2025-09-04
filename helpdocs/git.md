# Merge main (or other branch)
git fetch 
git stash 
git merge main 

# stage local changes 
git add path/to/file.txt 
git add -A 

# unstage local changes 
git reset path/to/file.txt 
git reset * 

# remove local changes 
# note this just dumps them to stash but you can restore them later 
git stash 

# discard changes for a file 
git chckout -- file_name 

# Stash 
git stash list 
git stash -n "my changes"
git stash clear 
git stash show stash@{0}

# clone
git clone git@github.com:sonatype/nexus-internal.git 
git clone git@github.com:sonatype/nexus-internal.git nexus-internal-karaf

# Discard all current changes and set back to HEAD
git reset --hard HEAD && git clean -fd

# custom script to add all and commit 
gitCommitAndPush



