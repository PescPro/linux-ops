Shell 变量

```shell
myvariable="hello world"
#输出变量值
echo $myvariable
```

1. 变量名第一个字符不能为$
2. 变量名和等号之间不能有空格
3. 变量名使用英文、数字和下划线，首个字符不能以数字开头
4. 变量名中间不能有空格
5. 不能使用bash的关键字

变量的使用

```shell
echo $myvariable
echo ${myvariable} #推荐使用
```

只读变量

```shell
#!/bin/bash
#使用 readonly 命令可以将变量定义为只读变量，只读变量的值不能被改变。
myvariable=1
readonly myvariable
myvariable=2
#输出
bash: myvariable: 只读变量
```

删除变量

```shell
#1.变量被删除后不能再次使用
myvariable=1
echo $myvariable
1
unset myvariable
echo $myvariable
#无任何输出

#2.unset 命令不能删除只读变量
myvariable=1
echo $myvariable
1
readonly myvariable
echo $myvariable
1
unset myvariable
bash: unset: myvariable: 无法取消设定: 只读 variable
```

