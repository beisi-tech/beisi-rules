# 项目开发编码规范

## commit 提交规范

| 类型     | 说明                                           |
| -------- | ---------------------------------------------- |
| feat     | 新增功能                                       |
| fix      | 修复 Bug                                       |
| docs     | 文档变更                                       |
| style    | 代码风格调整（不影响功能，比如空格、格式化等） |
| refactor | 代码重构（既不新增功能，也不修复 bug）         |
| perf     | 性能优化                                       |
| test     | 测试相关                                       |
| chore    | 构建或辅助工具变更（如依赖更新、构建脚本等）   |
| ci       | CI 配置更新                                    |
| build    | 打包构建相关                                   |
| revert   | 撤销上一次的提交                               |

**示范如下：**

```
feat: 支持用户使用手机号登录
fix: 修复微信支付回调问题
docs: 更新安装部署指南
style: 优化头部布局的代码缩进
refactor: 重构用户认证模块代码逻辑
perf: 优化列表渲染性能
test: 增加订单模块的单元测试
chore: 升级vue到最新版本
ci: 更新 Jenkins 流水线配置
build: 修改 Dockerfile，减小镜像体积
```

## 使用 **Prettier** 工具格式化代码

Prettier 工具使用方法如下：

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

# 关于 Dart

对于 Flutter 前端项目代码（Dart 语言）  
使用 Dart 自带的 **Dark format** 工具
