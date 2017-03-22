Git is a distributed version control system,
Git is free software distributed under the GPL.
Git has a mutable index called stage.
Git tracks changes of files.

2017.03.22学习廖雪峰的git教程日志：
命令行所有信息如下：

Administrator@G6WOK22J9NLIICT MINGW32 ~
$ pwd
/c/Documents and Settings/Administrator

Administrator@G6WOK22J9NLIICT MINGW32 ~
$ cd d:

Administrator@G6WOK22J9NLIICT MINGW32 /d
$ cd mwysgit/learngit
bash: cd: mwysgit/learngit: No such file or directory

Administrator@G6WOK22J9NLIICT MINGW32 /d
$ dir
360Downloads                 PHP\ Manual\ 2015中文手册.chm
360Rec                       RECYCLER
360安全浏览器下载            soft
APMServ5.2.6                 StormMedia
ExifDateEdit                 System\ Volume\ Information
ExifDateEdit.rar             Xiaomi
foxit\ reader.exe            李涛老师24集Photoshop调色教程
HDTunePro5.0_H_XiaZaiBa.zip  其他
hp\ p1108驱动盘              软件
hw\ ocr\ 图片文字识别        搜狗高速下载
msysgit                      王天注安考试资料转化
nodejs                       微积分超入门
oa所有插件安装2016.09.07     音乐
pdf\ to\ dwg                 音乐2
PDF转换为\ word工具          照片信息修改软件
photoshop7green              专业截屏Snagit9_HA_XiaZaiBa

Administrator@G6WOK22J9NLIICT MINGW32 /d
$ pwd
/d

Administrator@G6WOK22J9NLIICT MINGW32 /d
$ cd msysgit/learngit

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ dir
file1.txt  file2.txt  file3.txt  readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ cls
bash: cls: command not found

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ pwd
/d/msysgit/learngit

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ cat readme.txt
Git is a distributed version control system,
Git is free software distributed under the GPL.

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git log
commit b95a6c86a34013b1deef4e3076678e71d633459f
Author: mcc168 <mcc168@126.com>
Date:   Wed Mar 22 10:51:10 2017 +0800

    appedn GPL

commit 0166a7cda1c40f0d100ea7b27bbb7221371790e7
Author: mcc168 <mcc168@126.com>
Date:   Wed Mar 22 10:46:25 2017 +0800

    add distribute

commit 609b321f35c3077fa2aaa2362408d814689728eb
Author: mcc168 <mcc168@126.com>
Date:   Wed Mar 22 10:32:00 2017 +0800

    add 3 files

commit 58a770810b57c77f52ec41d09e272accedf78b3d
Author: mcc168 <mcc168@126.com>
Date:   Wed Mar 22 10:27:47 2017 +0800

    wrote a readme file

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git add readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        readme.txt.bak


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git add readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ cat readme.txt
Git is a distributed version control system,
Git is free software distributed under the GPL.
Git has a mutable called stage.
Git tracks changes.

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ cat readme.txt
Git is a distributed version control system,
Git is free software distributed under the GPL.
Git has a mutable called stage.
Git tracks changes.

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git commit -m "git tracks changes"
[master 98d5e51] git tracks changes
 1 file changed, 2 insertions(+)

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git diff HEAD --readme.txt
usage: git diff [<options>] [<commit> [<commit>]] [--] [<path>...]

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git diff HEAD --readme.txt diff --git a/readme.txt b/readme.txt
fatal: ambiguous argument 'diff': unknown revision or path not in the working tree.
Use '--' to separate paths from revisions, like this:
'git <command> [<revision>...] -- [<file>...]'

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git add readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git commit -m "second commit"
[master 57afe57] second commit
 1 file changed, 2 insertions(+), 2 deletions(-)

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git statue
git: 'statue' is not a git command. See 'git --help'.

Did you mean this?
        status

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git checkout -- readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git add readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        modified:   readme.txt

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        readme.txt.bak


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git reset HEAD readme.txt
Unstaged changes after reset:
M       readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        modified:   readme.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git checkout -- readme.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git add test.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git commit -m "add test.txt"
[master 7e919b8] add test.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 test.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ rm test.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes not staged for commit:
  (use "git add/rm <file>..." to update what will be committed)
  (use "git checkout -- <file>..." to discard changes in working directory)

        deleted:    test.txt

no changes added to commit (use "git add" and/or "git commit -a")

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git rm test.txt
rm 'test.txt'

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git checkout -- test.txt
error: pathspec 'test.txt' did not match any file(s) known to git.

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
Changes to be committed:
  (use "git reset HEAD <file>..." to unstage)

        deleted:    test.txt


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git commit -m "delete test.txt"
[master bfad1ec] delete test.txt
 1 file changed, 0 insertions(+), 0 deletions(-)
 delete mode 100644 test.txt

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git status
On branch master
nothing to commit, working directory clean

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config --get-all
error: wrong number of arguments
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config --get
error: wrong number of arguments
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config
usage: git config [<options>]

Config file location
    --global              use global config file
    --system              use system config file
    --local               use repository config file
    -f, --file <file>     use given config file
    --blob <blob-id>      read config from given blob object

Action
    --get                 get value: name [value-regex]
    --get-all             get all values: key [value-regex]
    --get-regexp          get values for regexp: name-regex [value-regex]
    --get-urlmatch        get value specific for the URL: section[.var] URL
    --replace-all         replace all matching variables: name value [value_regex]
    --add                 add a new variable: name value
    --unset               remove a variable: name [value-regex]
    --unset-all           remove all matches: name [value-regex]
    --rename-section      rename section: old-name new-name
    --remove-section      remove a section: name
    -l, --list            list all
    -e, --edit            open an editor
    --get-color           find the color configured: slot [default]
    --get-colorbool       find the color setting: slot [stdout-is-tty]

Type
    --bool                value is "true" or "false"
    --int                 value is decimal number
    --bool-or-int         value is --bool or --int
    --path                value is a path (file or directory name)

Other
    -z, --null            terminate values with NUL byte
    --name-only           show variable names only
    --includes            respect include directives on lookup
    --show-origin         show origin of config (file, standard input, blob, command line)


Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config --global user.name
mcc168

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config --global user
error: key does not contain a section: user
Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git config --global user.email
mcc168@126.com

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ pwd
/d/msysgit/learngit

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ ssh-keygen -t rsa -C "mcc168@126.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Documents and Settings/Administrator/.ssh/id_rsa):
Created directory '/c/Documents and Settings/Administrator/.ssh'.
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Documents and Settings/Administrator/.ssh/id_rsa.
Your public key has been saved in /c/Documents and Settings/Administrator/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:6nq9iwapJsYaBv1EqO9PomM+pAAA6Jq/6islKbRM8i4 mcc168@126.com
The key's randomart image is:
+---[RSA 2048]----+
|+                |
|o  .             |
|o . .            |
|o* .             |
|X+o ..  S        |
|O=ooo  .         |
|B*o.o...         |
|EO=o .o..        |
|@X=oo+o oo       |
+----[SHA256]-----+

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ ls -al ~/.ssh
total 5
drwxr-xr-x 1 Administrator 197121    0 三月 22 14:24 ./
drwxr-xr-x 1 Administrator 197121    0 三月 22 14:23 ../
-rw-r--r-- 1 Administrator 197121 1675 三月 22 14:24 id_rsa
-rw-r--r-- 1 Administrator 197121  396 三月 22 14:24 id_rsa.pub

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ eval $(ssh-agent -s)
Agent pid 5188

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ shh-add ~/.ssh/id_rsa
bash: shh-add: command not found

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git remote add origin https://github.com/mcc168/learngit.git

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$ git push -u origin master
Username for 'https://github.com': mcc168
Counting objects: 21, done.
Delta compression using up to 2 threads.
Compressing objects: 100% (19/19), done.
Writing objects: 100% (21/21), 1.68 KiB | 0 bytes/s, done.
Total 21 (delta 8), reused 0 (delta 0)
remote: Resolving deltas: 100% (8/8), done.
To https://github.com/mcc168/learngit.git
 * [new branch]      master -> master
Branch master set up to track remote branch master from origin.

Administrator@G6WOK22J9NLIICT MINGW32 /d/msysgit/learngit (master)
$
