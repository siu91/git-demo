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
## 从develop分支checkout新的功能分支进行开发，例如：`feature-discuss`
```bash
git checkout -b feature-discuss
```
