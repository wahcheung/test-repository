# test-repository
A repository for testing Git commands.

## git config

### 查看git仓库的设置

```sh
$ git config --list
```
### 设置git全局的用户名和邮箱

如果没有单独为某个仓库设置用户名和邮箱，则会使用这个全局设置作为初始值。

```sh
$ git config --global user.name huachang.gong
$ git config --global user.email huachang.gong@outlook.com
```

### 设置git当前仓库的用户名和邮箱

```sh
$ git config user.name huachang.gong
$ git config user.email huachang.gong@outlook.com
```

## git branch

### 新建分支并切换到新分支

```sh
$ git checkout -b test-branch
```

### 删除分支

```sh
$ git branch -d test-branch
```

## git fetch

### 拉取远程分支并创建本地分支

```sh
$ git fetch origin remote-branch:new-local-branch
```

如果需要在创建分支后立即切换，可以使用下面的命令:

```sh
$ git checkout -b new-local-branch remote-branch
```

## git merge

在多人合作开发的项目中，添加功能或者修复Bug时，一般新建分支，然后在新分支上开发，开发完成后再将新功能(修复)合并到主分支，这时往往需要用到`git merge`命令。

### 压缩提交日志

在一个新分支上开发，产生了多个commit，在将这些更改合并到主分支时，往往需要合并这些提交，这时候需要使用squash选项。

```sh
$ git merge --squash feature_branch
$ git commit -m "your commit log info"
```

## git push

### 新建远程分支

根据本地master分支创建远程develop分支:

```sh
$ git push origin master:develop
```

### 删除远程分支

```sh
$ git push origin --delete develop
```

或者

```sh
$ git push origin :develop
```

## git rebase

`git rebase`命令将提交到某一分支上的所有修改都移至另一分支上，就好像“重新播放”一样。

