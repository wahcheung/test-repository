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

如果需要在创建分支后立即切换，可以使用下面的命令

```sh
$ git checkout -b new-local-branch remote-branch
```
