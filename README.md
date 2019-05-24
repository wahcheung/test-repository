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
