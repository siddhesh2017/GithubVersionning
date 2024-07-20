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

git stash
changed to features/navbar branch commited changes there, switch to main and now
git stash apply
Got previous changes 
git add .
git commit -m "stash applied"




PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git init
Initialized empty Git repository in C:/Users/siddh/Desktop/Coding/WebDev/GitHubPractice/.git/
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git status -s
?? README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git status -s
AM README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "First commit(snapshot - 7 lines)"
[master (root-commit) 8d1ca17] First commit(snapshot - 7 lines)
 1 file changed, 6 insertions(+)
 create mode 100644 README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "Second commit(snapshot2 - 7 lines)"
[master 87f05d4] Second commit(snapshot2 - 7 lines)
 1 file changed, 2 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
87f05d4 (HEAD -> master) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git status -s
 M README.md
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "Third commit(snapshot2 - 7 lines)" 
[master 5b4549e] Third commit(snapshot2 - 7 lines)
 1 file changed, 3 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log -oneline
fatal: unrecognized argument: -oneline
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
5b4549e (HEAD -> master) Third commit(snapshot2 - 7 lines)
87f05d4 Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git reset --hard HEAD~1
HEAD is now at 87f05d4 Second commit(snapshot2 - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
87f05d4 (HEAD -> master) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git branch main
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git branch features/navbar
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git switch main
M       README.md
Switched to branch 'main'
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit  -m "fouth commit(main branch commit)"
[main a3a5165] fouth commit(main branch commit)
 1 file changed, 4 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
a3a5165 (HEAD -> main) fouth commit(main branch commit)
87f05d4 (master, features/navbar) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git switch features/navbar
Switched to branch 'features/navbar'
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "fifth commit on features/navbar branch"
[features/navbar cea80b5] fifth commit on features/navbar branch
 1 file changed, 6 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git switch main
Switched to branch 'main'
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
a3a5165 (HEAD -> main) fouth commit(main branch commit)
87f05d4 (master) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --graph  
* commit a3a5165453d9da3db0bc0fa6f4407fcbbce971e8 (HEAD -> main)
| Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| Date:   Sat Jul 20 13:59:29 2024 +0530
|
|     fouth commit(main branch commit)
|
* commit 87f05d4e03bc6889641656b9cf4397a2fe97b01e (master)
| Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| Date:   Sat Jul 20 13:54:16 2024 +0530
|
|     Second commit(snapshot2 - 7 lines)
|
* commit 8d1ca17d7c3e1b8c8b30cf6cabc933cd8472271f
  Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
  Date:   Sat Jul 20 13:53:22 2024 +0530

      First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git merge features/navbar
Auto-merging README.md
CONFLICT (content): Merge conflict in README.md
Automatic merge failed; fix conflicts and then commit the result.
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git status
On branch main
You have unmerged paths.
  (fix conflicts and run "git commit")
  (use "git merge --abort" to abort the merge)

Unmerged paths:
  (use "git add <file>..." to mark resolution)
        both modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git stash
README.md: needs merge
error: could not write index
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "6th commit merged both branch" 
[main db33fc8] 6th commit merged both branch
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git stash
Saved working directory and index state WIP on main: db33fc8 6th commit merged both branch
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git switch features/navbar
Switched to branch 'features/navbar'
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add.
git: 'add.' is not a git command. See 'git --help'.

The most similar command is
        add
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "7th commit from features/navbar branch"
[features/navbar 1d2049c] 7th commit from features/navbar branch
 1 file changed, 3 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
1d2049c (HEAD -> features/navbar) 7th commit from features/navbar branch
cea80b5 fifth commit on features/navbar branch
87f05d4 (master) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git switch main
Switched to branch 'main'
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git stash apply
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   README.md

no changes added to commit (use "git add" and/or "git commit -a")
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git add .
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git commit -m "stash applied" 
[main 1093158] stash applied
 1 file changed, 8 insertions(+), 1 deletion(-)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log -oneline
fatal: unrecognized argument: -oneline
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --oneline
1093158 (HEAD -> main) stash applied
db33fc8 6th commit merged both branch
cea80b5 fifth commit on features/navbar branch
a3a5165 fouth commit(main branch commit)
87f05d4 (master) Second commit(snapshot2 - 7 lines)
8d1ca17 First commit(snapshot - 7 lines)
PS C:\Users\siddh\Desktop\Coding\WebDev\GitHubPractice> git log --graph  
* commit 109315817a07053a71697e74700318554f46adbb (HEAD -> main)
| Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| Date:   Sat Jul 20 14:09:51 2024 +0530
|
|     stash applied
|
*   commit db33fc861333d7afca098ca64a4e9910924de50c
|\  Merge: a3a5165 cea80b5
| | Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| | Date:   Sat Jul 20 14:05:46 2024 +0530
| |
| |     6th commit merged both branch
| |
| * commit cea80b5f774311378f36342090799e4d351a7683
| | Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| | Date:   Sat Jul 20 14:01:39 2024 +0530
| |
| |     fifth commit on features/navbar branch
| |
* | commit a3a5165453d9da3db0bc0fa6f4407fcbbce971e8
|/  Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
|   Date:   Sat Jul 20 13:59:29 2024 +0530
|
|       fouth commit(main branch commit)
|
* commit 87f05d4e03bc6889641656b9cf4397a2fe97b01e (master)
| Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
| Date:   Sat Jul 20 13:54:16 2024 +0530
|
|     Second commit(snapshot2 - 7 lines)
|
* commit 8d1ca17d7c3e1b8c8b30cf6cabc933cd8472271f
  Author: siddhesh2017 <siddheshjagtap2017@gmail.com>
  Date:   Sat Jul 20 13:53:22 2024 +0530

      First commit(snapshot - 7 lines)
      