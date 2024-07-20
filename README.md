U - untracked files
A - added or stagged files (tracked)
C - commited files (snapshots/ checkpoints)

git init 
git status -s
git add README.md / git add .

//main branch
git log --oneline
git reset --hard HEAD~1

//features/navbar branch
git branch feature/navbar
git add. 
git commit -m "commit on features/navbar branch"
git switch main


**Both branches merged**