## Shell Basic

在后台执行 cmd 指令

```
cmd &
```

命令序列. 在同一行执行多个命令

```
cmd1 ; cmd2
```

在当前 shell 中以一组的形式执行多个命令

```
{ cmd1 ; cmd2 ; }
```

在子 shell 中以一组的形式执行多个命令

```
(cmd1 ; cmd2)
```

管道. 以 cmd1 的执行输出作为 cmd2 的输入

```
cmd1 | cmd2
```

命令替换. 以 cmd2 的执行输出作为 cmd1 的参数

```
cmd1 `cmd2`
```

POSIX 命令替换. 允许嵌套

```
cmd1 $(cmd2)
```

POSIX 算术替换. 将表达式 expression 的结果作为 cmd 的参数

```
cmd $((expression))
```

AND. 执行 cmd1, 然后执行 cmd2(如果 cmd1 执行成功的话). 如果 cmd1 执行失败, cmd2 则不会被执行

```
cmd1 && cmd2
```

OR. 要么执行 cmd1 要么执行 cmd2(如果 cmd1 执行失败的话). 如果 cmd1 执行成功, cmd2 则不会被执行

```
cmd1 || cmd2
```

NOT. 执行 cmd, 并且产生一个为 0 的退出状态码(如果 cmd 的退出状态是非零的话). 否则, 产生一个非零的退出状态码(如果 cmd 的退出状态是零的话).

```
! cmd
```

