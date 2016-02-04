# git-demo
使用git和github进行协同开发流程

---------------------------------
## 在GItHub上新建一个repository，初始化创建两个分支：`master`、`develop`
![图](src\img\create_master_develop_branch.png)
## 在本地clone仓库并checkout到develop分支
```bash
$ git clone git@github.com:gongice/git-demo.git
loning into 'git-demo'...
remote: Counting objects: 9, done.
remote: Compressing objects: 100% (6/6), done.
remote: Total 9 (delta 0), reused 0 (delta 0), pack-reused 0
Receiving objects: 100% (9/9), done.
Checking connectivity... done.
                /E/Workstation/Github
$ cd git-demo/
                /E/Workstation/Github/git-demo (master)
$ git branch
master
                /E/Workstation/Github/git-demo (master)
$ git checkout develop
 ranch develop set up to track remote branch develop from origin.
 Switched to a new branch 'develop'
                /E/Workstation/Github/git-demo (develop)
```
## 检查develop分支是否有更新，有更新则提交。
```bash
$ git status
n branch develop
Your branch is up-to-date with 'origin/develop'.
Changes not staged for commit:
(use "git add <file>..." to update what will be committed)
(use "git checkout -- <file>..." to discard changes in working directory)
      modified:   README.md
Untracked files:
(use "git add <file>..." to include in what will be committed)
      src/
no changes added to commit (use "git add" and/or "git commit -a")

                /E/Workstation/Github/git-demo (develop)
$ git add *
                /E/Workstation/Github/git-demo (develop)
$ git status
n branch develop
Your branch is up-to-date with 'origin/develop'.
Changes to be committed:
(use "git reset HEAD <file>..." to unstage)
      modified:   README.md
      new file:   src/img/create_master_develop_branch.png
                /E/Workstation/Github/git-demo (develop)
$ git commit -m "add src/img/create_master_develop_branch.png and update README.md"
develop 27ccc0c] add src/img/create_master_develop_branch.png and update README.md
2 files changed, 28 insertions(+)
create mode 100644 src/img/create_master_develop_branch.png
                /E/Workstation/Github/git-demo (develop)
$ git push origin develop
ounting objects: 8, done.
Delta compression using up to 4 threads.
Compressing objects: 100% (5/5), done.
```
## 从develop分支checkout新的功能分支进行开发，例如：`feature-discuss`
```bash
git checkout -b feature-discuss
```
