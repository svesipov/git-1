Air-Sergey:GitHub Sergey$ mkdir git-1-repA

Air-Sergey:GitHub Sergey$ cd git-1-repA/

Air-Sergey:git-1-repA Sergey$ git init

Initialized empty Git repository in /Users/Sergey/GitHub/git-1-repA/.git/

Air-Sergey:git-1-repA Sergey$ echo 'File A' > A.txt

Air-Sergey:git-1-repA Sergey$ echo 'File B' > B.txt

Air-Sergey:git-1-repA Sergey$ git add A.txt

Air-Sergey:git-1-repA Sergey$ git add B.txt

Air-Sergey:git-1-repA Sergey$ git commit -m 'Task1.02'

[master (root-commit) e4bc7fb] Task1.02

 2 files changed, 2 insertions(+)

 create mode 100644 A.txt

 create mode 100644 B.txt

Air-Sergey:git-1-repA Sergey$ git branch branch1

Air-Sergey:git-1-repA Sergey$ cd ..

Air-Sergey:GitHub Sergey$ git clone git-1-repA/ git-1-repB/

Cloning into 'git-1-repB'...

done.

Air-Sergey:GitHub Sergey$ cd git-1-repB

Air-Sergey:git-1-repB Sergey$ git checkout branch1

Branch branch1 set up to track remote branch branch1 from origin.

Switched to a new branch 'branch1'

Air-Sergey:git-1-repB Sergey$ echo 'File C' > C.txt

Air-Sergey:git-1-repB Sergey$ git add C.txt

Air-Sergey:git-1-repB Sergey$ git commit -m 'Task1.05'

[branch1 8541f52] Task1.05

 1 file changed, 1 insertion(+)

 create mode 100644 C.txt

Air-Sergey:git-1-repB Sergey$ git push

Air-Sergey:git-1-repB Sergey$ cd ../git-1-repA/

Air-Sergey:git-1-repA Sergey$ git checkout branch1

Already on 'branch1'

Air-Sergey:git-1-repA Sergey$ vim C.txt

Air-Sergey:git-1-repA Sergey$ cd ../git-1-repB/

Air-Sergey:git-1-repB Sergey$ git checkout branch1

Already on 'branch1'

Your branch is up-to-date with 'origin/branch1'.

Air-Sergey:git-1-repB Sergey$ vim C.txt

Air-Sergey:git-1-repB Sergey$ cd ../git-1-repA/

Air-Sergey:git-1-repA Sergey$ git add C.txt

Air-Sergey:git-1-repA Sergey$ git commit -m 'Task1.07'

[branch1 68b59e1] Task1.07

 1 file changed, 1 insertion(+), 1 deletion(-)

Air-Sergey:git-1-repA Sergey$ cd ../git-1-repB/

Air-Sergey:git-1-repB Sergey$ git add C.txt

Air-Sergey:git-1-repB Sergey$ git commit -m 'Task1.08'

[branch1 cd7f3e3] Task1.08

 1 file changed, 1 insertion(+), 1 deletion(-)

Air-Sergey:git-1-repB Sergey$ git fetch origin

remote: Counting objects: 5, done.

remote: Compressing objects: 100% (2/2), done.

remote: Total 3 (delta 1), reused 0 (delta 0)

Unpacking objects: 100% (3/3), done.

From /Users/Sergey/GitHub/git-1-repA

   8541f52..68b59e1  branch1    -> origin/branch1

Air-Sergey:git-1-repB Sergey$ git pull

Auto-merging C.txt

CONFLICT (content): Merge conflict in C.txt

Automatic merge failed; fix conflicts and then commit the result.

Air-Sergey:git-1-repB Sergey$ git mergetool

Air-Sergey:git-1-repB Sergey$ git commit -m 'Task1.10'

[branch1 9e06042] Task1.10

Air-Sergey:git-1-repB Sergey$ cd ../git-1-repA/

Air-Sergey:git-1-repA Sergey$ git remote add remoteB ../git-1-repB/

Air-Sergey:git-1-repA Sergey$ git fetch remoteB

Air-Sergey:git-1-repA Sergey$ git pull remoteB branch1

From ../git-1-repB

 * branch            branch1    -> FETCH_HEAD

Updating 68b59e1..9e06042

Fast-forward
 
 C.txt | 4 ++++
 
 1 file changed, 4 insertions(+)

