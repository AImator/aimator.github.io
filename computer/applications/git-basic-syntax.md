## [Git 基础语法](./git-basic-syntax)

##### *Made by* [AImator.com]()

本章主要介绍了 Git 的基础语法。

### 初始设置

#### 设置用户名

```git
$ git config --global user.name "username"
```

#### 设置邮箱

```git
$ git config --global user.email user@server
```

#### 设置本用户快捷短语

```git
$ git config --global alalias.st status
$ git config --global alalias.ci commit
$ git config --global alalias.co checkout
$ git config --global alalias.br branch
```

#### 开启输出颜色显示

```git
$ git config --global color.ui true
```

### 创建版本库及第一次提交

#### 创建版本库

进入项目文件夹执行创建版本库命令

```git
$ cd demo
$ git init
```

使用项目文件夹绝对路径作为创建版本库命令的参数

```git
$ git init demo
```

#### 添加新文件至版本库

```git
$ git add newfile
```

#### 进行说明并完成提交

```git
$ git commit -m "description"
```