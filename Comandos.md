
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


User@DESKTOP-93641C4 MINGW64 ~
$ g clone git@github.com:luisfguga/Curso-GitHub.git git-course-clone
bash: g: command not found

User@DESKTOP-93641C4 MINGW64 ~
$ g clone git@github.com:luisfguga/Curso-GitHub.git Curso-GitHub-clone
bash: g: command not found

User@DESKTOP-93641C4 MINGW64 ~
$ git clone git@github.com:luisfguga/Curso-GitHub.git Curso-GitHub-clone
Cloning into 'Curso-GitHub-clone'...
The authenticity of host 'github.com (20.201.28.151)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Please type 'yes', 'no' or the fingerprint:eseses/no/[fingerprint])?
Please type 'yes', 'no' or the fingerprint: yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
remote: Enumerating objects: 12, done.
remote: Counting objects: 100% (12/12), done.
remote: Compressing objects: 100% (8/8), done.
remote: Total 12 (delta 2), reused 12 (delta 2), pack-reused 0
Receiving objects: 100% (12/12), done.
Resolving deltas: 100% (2/2), done.

User@DESKTOP-93641C4 MINGW64 ~
$ ls
'3D Objects'/
'Ambiente de Impressão'@
'Ambiente de Rede'@
 AppData/
'Configurações Locais'@
 Contacts/
 Cookies@
 Curso-GitHub-clone/
'Dados de Aplicativos'@
 Desktop/
 Documents/
 Downloads/
 Favorites/
 IntelGraphicsProfiles/
 Links/
'Menu Iniciar'@
'Meus Documentos'@
 Modelos@
 Music/
 NTUSER.DAT
 NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TM.blf
 NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TMContainer00000000000000000001.regtrans-ms
 NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TMContainer00000000000000000002.regtrans-ms
 OneDrive/
 Pictures/
 Recent@
'Saved Games'/
 Searches/
 SendTo@
 Videos/
 eclipse/
 eclipse-workspace/
 git-course/
 ntuser.dat.LOG1
 ntuser.dat.LOG2
 ntuser.ini

User@DESKTOP-93641C4 MINGW64 ~
$ cd Curso-GitHub-clone

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (main)
$ ls
Comandos.md  Readme.md

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (main)
$ more Readme.md
bash: more: command not found

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (main)
$ ls
Comandos.md  Readme.md

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (main)
$ git checkout -b testebranch
Switched to a new branch 'testebranch'

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (testebranch)
$ cd..
bash: cd..: command not found

User@DESKTOP-93641C4 MINGW64 ~/Curso-GitHub-clone (testebranch)
$ cd ..

User@DESKTOP-93641C4 MINGW64 ~
$ cd git-course/

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git checkout -b criandoBranch
Switched to a new branch 'criandoBranch'

User@DESKTOP-93641C4 MINGW64 ~/git-course (criandoBranch)
$ git branch
* criandoBranch
  main

User@DESKTOP-93641C4 MINGW64 ~/git-course (criandoBranch)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git checkout criandoBranch
Switched to branch 'criandoBranch'

User@DESKTOP-93641C4 MINGW64 ~/git-course (criandoBranch)
$ git branch -d criandoBranch
error: cannot delete branch 'criandoBranch' used by worktree at 'C:/Users/User/git-course'

User@DESKTOP-93641C4 MINGW64 ~/git-course (criandoBranch)
$ git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git branch -d criandoBranch
Deleted branch criandoBranch (was ef3e8b2).

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ vi Comandos.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ mkdir rebase-merge

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ cd rebase-merge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (main)
$ git init
Initialized empty Git repository in C:/Users/User/git-course/rebase-merge/.git/

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ ls

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ vim arq1

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git status
On branch master

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        arq1

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git add arq1
warning: in the working copy of 'arq1', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git commit -am "adicionando primeiro arquivo"
[master (root-commit) 0528a93] adicionando primeiro arquivo
 1 file changed, 1 insertion(+)
 create mode 100644 arq1

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git checkout -b branch1
Switched to a new branch 'branch1'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ vim arq2

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git add arq2
warning: in the working copy of 'arq2', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git commit -m "criando arquivo 2"
[branch1 ef8ce82] criando arquivo 2
 1 file changed, 1 insertion(+)
 create mode 100644 arq2

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ vim arq3

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git add arq3
warning: in the working copy of 'arq3', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git commit -m "arquivo 3"
[branch1 3e511b8] arquivo 3
 1 file changed, 1 insertion(+)
 create mode 100644 arq3

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkout main
error: pathspec 'main' did not match any file(s) known to git

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git branch
* branch1
  master

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkou master
git: 'checkou' is not a git command. See 'git --help'.

The most similar command is
        checkout

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkout master
Switched to branch 'master'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ vim arq4

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git merge arq2
merge: arq2 - not something we can merge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git merge branch1
Updating 0528a93..3e511b8
Fast-forward
 arq2 | 1 +
 arq3 | 1 +
 2 files changed, 2 insertions(+)
 create mode 100644 arq2
 create mode 100644 arq3

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ ls
arq1  arq2  arq3  arq4

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log
commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> master, branch1)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> master, branch1)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git checkout -b branch2
Switched to a new branch 'branch2'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch2)
$ vim arq5

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch2)
$ git log
commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> branch2, master, branch1)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch2)
$ git branch
  branch1
* branch2
  master

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch2)
$ git checkout -b branch3
Switched to a new branch 'branch3'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ vim arq5

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ ls
arq1  arq2  arq3  arq4  arq5

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ vim arq6

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git log --graph
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> branch3, master, branch2, branch1)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git add arq6
warning: in the working copy of 'arq6', LF will be replaced by CRLF the next time Git touches it


User@DESKTOP-93641C4 MINGW64 ~
$ ls
'3D Objects'/             'Dados de Aplicativos'@  'Meus Documentos'@                                                                              Pictures/            git-course/
'Ambiente de Impressão'@   Desktop/                 Modelos@                                                                                       Recent@              ntuser.dat.LOG1
'Ambiente de Rede'@        Documents/               Music/                                                                                        'Saved Games'/        ntuser.dat.LOG2
 AppData/                  Downloads/               NTUSER.DAT                                                                                     Searches/            ntuser.ini
'Configurações Locais'@    Favorites/               NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TM.blf                                        SendTo@
 Contacts/                 IntelGraphicsProfiles/   NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TMContainer00000000000000000001.regtrans-ms   Videos/
 Cookies@                  Links/                   NTUSER.DAT{53b39e88-18c4-11ea-a811-000d3aa4692b}.TMContainer00000000000000000002.regtrans-ms   eclipse/
 Curso-GitHub-clone/      'Menu Iniciar'@           OneDrive/                                                                                      eclipse-workspace/

User@DESKTOP-93641C4 MINGW64 ~
$ cd git-course

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ ls
Comandos.md  Readme.md  rebase-merge/

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ cd rebase-merge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ cd ..

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ vim Comandos.md

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ cd rebase-merge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git branch
  branch1
  branch2
* branch3
  master

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git status
On branch branch3
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
        new file:   arq6

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        arq4
        arq5


User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git commit -m "testando rebase"
[branch3 b91070d] testando rebase
 1 file changed, 1 insertion(+)
 create mode 100644 arq6

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git log --graph
* commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (HEAD -> branch3)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:33:51 2023 -0300
|
|     testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (master, branch2, branch1)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git checkout main
error: pathspec 'main' did not match any file(s) known to git

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch3)
$ git checkout master
Switched to branch 'master'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log
commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> master, branch2, branch1)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (HEAD -> master, branch2, branch1)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ vim arq7

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git add arq7
warning: in the working copy of 'arq7', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git commit -m "arquivo setimo"
[master 07af820] arquivo setimo
 1 file changed, 1 insertion(+)
 create mode 100644 arq7

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log
commit 07af8200fcb78a05083f2e17e80f7c8749ca156c (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:36:45 2023 -0300

    arquivo setimo

commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2, branch1)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git rebase rebase-merge
fatal: invalid upstream 'rebase-merge'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git rebase branch3
Successfully rebased and updated refs/heads/master.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
* commit a8fdf229a595c3594da4651c5d00110a103b3e34 (HEAD -> master)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:36:45 2023 -0300
|
|     arquivo setimo
|
* commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:33:51 2023 -0300
|
|     testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2, branch1)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git checkout branch1
Switched to branch 'branch1'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ vim arquivoMerge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git add arquivoMerge
warning: in the working copy of 'arquivoMerge', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git commit -m "tentando de novo dar merge"
[branch1 254d718] tentando de novo dar merge
 1 file changed, 1 insertion(+)
 create mode 100644 arquivoMerge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git status
On branch branch1
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        arq4
        arq5

nothing added to commit but untracked files present (use "git add" to track)

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git add arq4
warning: in the working copy of 'arq4', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git add arq5
warning: in the working copy of 'arq5', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git commit -am "colocando os de antes"
[branch1 12800b4] colocando os de antes
 2 files changed, 4 insertions(+)
 create mode 100644 arq4
 create mode 100644 arq5

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git log
commit 12800b43b5663961f5e72de9c35e2b5ff467bfeb (HEAD -> branch1)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:46:48 2023 -0300

    colocando os de antes

commit 254d718f7f76708a602a8d5b37e585ab12ff464d
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:46:08 2023 -0300

    tentando de novo dar merge

commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkou master
git: 'checkou' is not a git command. See 'git --help'.

The most similar command is
        checkout

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkout master
Switched to branch 'master'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
* commit a8fdf229a595c3594da4651c5d00110a103b3e34 (HEAD -> master)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:36:45 2023 -0300
|
|     arquivo setimo
|
* commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:33:51 2023 -0300
|
|     testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ vim arquivoMain

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git add arquivoMain
warning: in the working copy of 'arquivoMain', LF will be replaced by CRLF the next time Git touches it

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git commit -m "arquivoMain"
[master bd5c85d] arquivoMain
 1 file changed, 1 insertion(+)
 create mode 100644 arquivoMain

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log
commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:49:26 2023 -0300

    arquivoMain

commit a8fdf229a595c3594da4651c5d00110a103b3e34
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:36:45 2023 -0300

    arquivo setimo

commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:33:51 2023 -0300

    testando rebase

commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
* commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a (HEAD -> master)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:49:26 2023 -0300
|
|     arquivoMain
|
* commit a8fdf229a595c3594da4651c5d00110a103b3e34
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:36:45 2023 -0300
|
|     arquivo setimo
|
* commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:33:51 2023 -0300
|
|     testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git merge branch1
hint: Waiting for your editor to close the file... error: cannot spawn s: No such file or directory
error: unable to start editor 's'
Not committing merge; use 'git commit' to complete the merge.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git status
On branch master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        new file:   arq4
        new file:   arq5
        new file:   arquivoMerge


User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git commit
hint: Waiting for your editor to close the file... error: cannot spawn s: No such file or directory
error: unable to start editor 's'
Please supply the message using either -m or -F option.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git status
On branch master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        new file:   arq4
        new file:   arq5
        new file:   arquivoMerge


User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git diff

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git merge branch1
fatal: You have not concluded your merge (MERGE_HEAD exists).
Please, commit your changes before you merge.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git status
On branch master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        new file:   arq4
        new file:   arq5
        new file:   arquivoMerge


User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git log
commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a (HEAD -> master)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:49:26 2023 -0300

    arquivoMain

commit a8fdf229a595c3594da4651c5d00110a103b3e34
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:36:45 2023 -0300

    arquivo setimo

commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:33:51 2023 -0300

    testando rebase

commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:17:47 2023 -0300

    arquivo 3

commit ef8ce82c23278d344cf8e6cc3f19516e24165046
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:16:44 2023 -0300

    criando arquivo 2

commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
Date:   Fri Dec 8 16:14:40 2023 -0300

    adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git log --graph
* commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a (HEAD -> master)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:49:26 2023 -0300
|
|     arquivoMain
|
* commit a8fdf229a595c3594da4651c5d00110a103b3e34
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:36:45 2023 -0300
|
|     arquivo setimo
|
* commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:33:51 2023 -0300
|
|     testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
* commit 0528a93ed11e6f5d3c765ebcc8c70a34bc4da0cd
  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
  Date:   Fri Dec 8 16:14:40 2023 -0300

      adicionando primeiro arquivo

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git checkou branch1
git: 'checkou' is not a git command. See 'git --help'.

The most similar command is
        checkout

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git checkout branch1
Switched to branch 'branch1'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git status
On branch branch1
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (branch1)
$ git checkout master
Switched to branch 'master'

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git status
On branch master
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git merge branch1
hint: Waiting for your editor to close the file... error: cannot spawn s: No such file or directory
error: unable to start editor 's'
Not committing merge; use 'git commit' to complete the merge.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git status
On branch master
All conflicts fixed but you are still merging.
  (use "git commit" to conclude merge)

Changes to be committed:
        new file:   arq4
        new file:   arq5
        new file:   arquivoMerge


User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git commit
hint: Waiting for your editor to close the file... error: cannot spawn s: No such file or directory
error: unable to start editor 's'
Please supply the message using either -m or -F option.

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git commit -am
error: switch `m' requires a value

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git commit -m
error: switch `m' requires a value

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master|MERGING)
$ git commit -m "tentando consertar erro"
[master dd685f2] tentando consertar erro

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git status
On branch master
nothing to commit, working tree clean

User@DESKTOP-93641C4 MINGW64 ~
$ cd git-course

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ cd rebase-merge

User@DESKTOP-93641C4 MINGW64 ~/git-course/rebase-merge (master)
$ git log --graph
*   commit dd685f2f9b768714bb1a37778b63d46d4c7128bc (HEAD -> master)
|\  Merge: bd5c85d 12800b4
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:55:32 2023 -0300
| |
| |     tentando consertar erro
| |
| * commit 12800b43b5663961f5e72de9c35e2b5ff467bfeb (branch1)
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:46:48 2023 -0300
| |
| |     colocando os de antes
| |
| * commit 254d718f7f76708a602a8d5b37e585ab12ff464d
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:46:08 2023 -0300
| |
| |     tentando de novo dar merge
| |
* | commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:49:26 2023 -0300
| |
:...skipping...
*   commit dd685f2f9b768714bb1a37778b63d46d4c7128bc (HEAD -> master)
|\  Merge: bd5c85d 12800b4
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:55:32 2023 -0300
| |
| |     tentando consertar erro
| |
| * commit 12800b43b5663961f5e72de9c35e2b5ff467bfeb (branch1)
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:46:48 2023 -0300
| |
| |     colocando os de antes
| |
| * commit 254d718f7f76708a602a8d5b37e585ab12ff464d
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:46:08 2023 -0300
| |
| |     tentando de novo dar merge
| |
* | commit bd5c85d6a94fff6c3da349c031c7d6b53c41a33a
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:49:26 2023 -0300
| |
| |     arquivoMain
| |
* | commit a8fdf229a595c3594da4651c5d00110a103b3e34
| | Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| | Date:   Fri Dec 8 16:36:45 2023 -0300
| |
| |     arquivo setimo
| |
* | commit b91070ded3ab67e0ccb1afdbff39e64c882c94ff (branch3)
|/  Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
|   Date:   Fri Dec 8 16:33:51 2023 -0300
|
|       testando rebase
|
* commit 3e511b8d5763541a75a72fb85b7d0dda8173c8a5 (branch2)
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:17:47 2023 -0300
|
|     arquivo 3
|
* commit ef8ce82c23278d344cf8e6cc3f19516e24165046
| Author: Luis Cunha <luis_fernando_gug@yahoo.com.br>
| Date:   Fri Dec 8 16:16:44 2023 -0300
|
|     criando arquivo 2
|
User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git config --global alias.s status

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git config --global alias.g git

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ g s
bash: g: command not found

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git s
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git tag -a 1.0.0 -m "curso finalizado"

User@DESKTOP-93641C4 MINGW64 ~/git-course (main)
$ git push origin main --tags
Enumerating objects: 1, done.
Counting objects: 100% (1/1), done.
Writing objects: 100% (1/1), 176 bytes | 176.00 KiB/s, done.
Total 1 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/luisfguga/Curso-GitHub.git
 * [new tag]         1.0.0 -> 1.0.0

