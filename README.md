> mkdir git-1-repA

> cd git-1-repA/

> git init

Initialized empty Git repository in /Users/Sergey/GitHub/git-1-repA/.git/

> echo 'File A' > A.txt

> echo 'File B' > B.txt

> git add A.txt

> git add B.txt

> git commit -m 'Task1.02'

[master (root-commit) e4bc7fb] Task1.02

 2 files changed, 2 insertions(+)

 create mode 100644 A.txt

 create mode 100644 B.txt
 

> git branch branch1

> cd ..

> git clone git-1-repA/ git-1-repB/

Cloning into 'git-1-repB'...

done.

> cd git-1-repB

> git checkout branch1

Branch branch1 set up to track remote branch branch1 from origin.

Switched to a new branch 'branch1'

> echo 'File C' > C.txt

> git add C.txt

> git commit -m 'Task1.05'

[branch1 8541f52] Task1.05

 1 file changed, 1 insertion(+)

 create mode 100644 C.txt

> git push

> cd ../git-1-repA/

> git checkout branch1

Already on 'branch1'

> vim C.txt

> cd ../git-1-repB/

> git checkout branch1

Already on 'branch1'

Your branch is up-to-date with 'origin/branch1'.

> vim C.txt

> cd ../git-1-repA/

> git add C.txt

> git commit -m 'Task1.07'

[branch1 68b59e1] Task1.07

 1 file changed, 1 insertion(+), 1 deletion(-)

> cd ../git-1-repB/

> git add C.txt

> git commit -m 'Task1.08'

[branch1 cd7f3e3] Task1.08

 1 file changed, 1 insertion(+), 1 deletion(-)

> git fetch origin

remote: Counting objects: 5, done.

remote: Compressing objects: 100% (2/2), done.

remote: Total 3 (delta 1), reused 0 (delta 0)

Unpacking objects: 100% (3/3), done.

From /Users/Sergey/GitHub/git-1-repA

   8541f52..68b59e1  branch1    -> origin/branch1

> git pull

Auto-merging C.txt

CONFLICT (content): Merge conflict in C.txt

Automatic merge failed; fix conflicts and then commit the result.

> git mergetool

> git commit -m 'Task1.10'

[branch1 9e06042] Task1.10

> cd ../git-1-repA/

> git remote add remoteB ../git-1-repB/

> git fetch remoteB

> git pull remoteB branch1

From ../git-1-repB

 * branch            branch1    -> FETCH_HEAD

Updating 68b59e1..9e06042

Fast-forward
 
 C.txt | 4 ++++
 
 1 file changed, 4 insertions(+)

