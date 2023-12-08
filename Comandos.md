
User@DESKTOP-93641C4 MINGW64 ~
$ git config --global user.name "Luis Cunha"

User@DESKTOP-93641C4 MINGW64 ~
$ git config --global user.email "luis_fernando_gug@yahoo.com.br"

User@DESKTOP-93641C4 MINGW64 ~
$ git config --global core.editor s

User@DESKTOP-93641C4 MINGW64 ~
$ git config user.name
Luis Cunha

User@DESKTOP-93641C4 MINGW64 ~
$ git config corre.editor

User@DESKTOP-93641C4 MINGW64 ~
$ git config core.editor
s

User@DESKTOP-93641C4 MINGW64 ~
$ git config --list
diff.astextplain.textconv=astextplain
filter.lfs.clean=git-lfs clean -- %f
filter.lfs.smudge=git-lfs smudge -- %f
filter.lfs.process=git-lfs filter-process
filter.lfs.required=true
http.sslbackend=openssl
http.sslcainfo=C:/Program Files/Git/mingw64/etc/ssl/certs/ca-bundle.crt
core.autocrlf=true
core.fscache=true
core.symlinks=false
pull.rebase=false
credential.helper=manager
credential.https://dev.azure.com.usehttppath=true
init.defaultbranch=master
user.name=Luis Cunha
user.email=luis_fernando_gug@yahoo.com.br
core.editor=s

User@DESKTOP-93641C4 MINGW64 ~
$ mkdir git-course

User@DESKTOP-93641C4 MINGW64 ~
$ cd git-course/

User@DESKTOP-93641C4 MINGW64 ~/git-course
$ git init
Initialized empty Git repository in C:/Users/User/git-course/.git/

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ ls -la
total 16
drwxr-xr-x 1 User 197121 0 Dec  6 15:34 ./
drwxr-xr-x 1 User 197121 0 Dec  6 15:31 ../
drwxr-xr-x 1 User 197121 0 Dec  6 15:34 .git/

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ cd .git/

User@DESKTOP-93641C4 MINGW64 ~/git-course/.git (GIT_DIR!)
$ ls
HEAD  config  description  hooks/  info/  objects/  refs/

User@DESKTOP-93641C4 MINGW64 ~/git-course/.git (GIT_DIR!)
$ cd..
bash: cd..: command not found

User@DESKTOP-93641C4 MINGW64 ~/git-course/.git (GIT_DIR!)
$ cd ..

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vi Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ ls
Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vi Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ ls
Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        Readme.md

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vim Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git add Readme.md
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vim Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git add Readme.md
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git comit -m "Add Reame.md"
git: 'comit' is not a git command. See 'git --help'.

The most similar command is
        commit

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git comit -m "Add Readme.mr"
git: 'comit' is not a git command. See 'git --help'.

The most similar command is
        commit

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
        new file:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git commit -m "Add Readme.md"
[master (root-commit) 216ac50] Add Readme.md
 1 file changed, 5 insertions(+)
 create mode 100644 Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log
commit 216ac50c428b21456ea4e291ef09181daa403430 (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 15:48:28 2023 -0300

    Add Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log --decorate
commit 216ac50c428b21456ea4e291ef09181daa403430 (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 15:48:28 2023 -0300

    Add Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log --author == "Luis"
fatal: ambiguous argument 'Luis': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log --author="luis"
commit 216ac50c428b21456ea4e291ef09181daa403430 (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 15:48:28 2023 -0300

    Add Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git short log
git: 'short' is not a git command. See 'git --help'.

The most similar command is
        shortlog

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git shortlog
Luis Cunha (1):
      Add Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log graph
fatal: ambiguous argument 'graph': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git loggraph
git: 'loggraph' is not a git command. See 'git --help'.

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log --graph
* commit 216ac50c428b21456ea4e291ef09181daa403430 (HEAD -> master)
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Wed Dec 6 15:48:28 2023 -0300

      Add Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git show^C

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git show ^[[200~216ac50c428b21456ea4e291ef09181daa403430~

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git show 216ac50c428b21456ea4e291ef09181daa403430
commit 216ac50c428b21456ea4e291ef09181daa403430 (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 15:48:28 2023 -0300

    Add Readme.md

diff --git a/Readme.md b/Readme.md
new file mode 100644
index 0000000..a61b4af
--- /dev/null
+++ b/Readme.md
@@ -0,0 +1,5 @@
+Github
+
+Arquivo para aula de Github
+
+modificando arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vim Readme.me

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vi Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
diff --git a/Readme.md b/Readme.md
index a61b4af..33b337e 100644
--- a/Readme.md
+++ b/Readme.md
@@ -3,3 +3,5 @@ Github
 Arquivo para aula de Github

 modificando arquivo
+
+verificar mudanças

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git add Readme.md
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff --name-only

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vi Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
diff --git a/Readme.md b/Readme.md
index 33b337e..1365822 100644
--- a/Readme.md
+++ b/Readme.md
@@ -5,3 +5,5 @@ Arquivo para aula de Github
 modificando arquivo

 verificar mudanças
+
+ok, verificado

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff --name-only
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
diff --git a/Readme.md b/Readme.md
index 33b337e..1365822 100644
--- a/Readme.md
+++ b/Readme.md
@@ -5,3 +5,5 @@ Arquivo para aula de Github
 modificando arquivo

 verificar mudanças
+
+ok, verificado

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff --name-only
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ g s
bash: g: command not found

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git add Readme.md
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git commit -m "editanto"
[master be73acb] editanto
 1 file changed, 4 insertions(+)

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ vim Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git add Readme.md
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        modified:   Readme.md


User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git reset HEAD Readme.md
Unstaged changes after reset:
M       Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff
warning: in the working copy of 'Readme.md', LF will be replaced by CRLF the next time Git touches it
diff --git a/Readme.md b/Readme.md
index 1365822..14cb67e 100644
--- a/Readme.md
+++ b/Readme.md
@@ -7,3 +7,6 @@ modificando arquivo
 verificar mudanças

 ok, verificado
+
+
+retirarndo modify

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git restore
fatal: you must specify path(s) to restore

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Readme.md

no changes added to commit (use "git add" and/or "git commit -a")

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git restore Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git statuts
git: 'statuts' is not a git command. See 'git --help'.

The most similar command is
        status

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git status
On branch master
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git diff

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$ git log
commit be73acb4372f4cf4c28a8c612f24aa2e4494f325 (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 16:03:26 2023 -0300

    editanto

commit 216ac50c428b21456ea4e291ef09181daa403430
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Wed Dec 6 15:48:28 2023 -0300

    Add Readme.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (master)
$



