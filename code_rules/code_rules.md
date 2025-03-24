# 项目开发编码规范 

统一使用 **Prettier** 工具格式化代码    

Prettier 工具使用方法如下：  

## Prettier 简明使用教程

### 获取 Prettier

全局安装 Prettier。

```bash
npm install -g prettier

yarn global add prettier

pnpm i -g prettier
```

### 使用 Prettier

打开你的**终端 / Terminal / 命令行**，不管在 IDE 的终端里还是在系统的 cmd / powershell / terminal 都行。

为了了解 Prettier 的完整功能列表，我们可以直接运行其 help 命令。

```bash
prettier -h
```

但常用的其实就两个：**检查** 和 **改正**。用法也很简单，对 prettier 传入对应的 flag 就可以使用了。

比如我们需要检查当前所在文件夹的全部文件，我们可以直接运行：

```bash
prettier . -c
```

这个命令的意思是：检查当前所在文件夹的全部文件，然后根据配置文件中的规则，检查出错的地方，然后在控制台输出文件名和检查结果。

如果 WARN 较多，则说明文件存在格式问题，可以直接修正。如果出现 ERROR 则通常意味着文件出现格式错误（比如没有关闭 Tag），需要自行手动修正。

直接修正则需要运行 `-w` 参数：

```bash
prettier . -w
```

这个指令会直接将当前目录下的所有文件进行文件格式修改（直接写入）。

不过在通常的情况下我们一般不使用这样的修改，而是指定好需要修改的文件位置（也就是 `.` 的位置）

比如我们在当前工程的 `前端` 文件夹内，我们需要格式化前端工程内 `pages` 文件夹下的所有文件，可以直接运行:

```bash
prettier .\pages -w
```

同理，你也可以指定 prettier 修改特定文件。

```bash
prettier .\index.json -w
```
  
# 关于Dart
对于 Flutter 前端项目代码（Dart 语言）  
使用Dart自带的 **Dark format** 工具