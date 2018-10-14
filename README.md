# git 的一些规范

## git commit

Commit message 的格式

```bash
<type>(<scope>): <subject>
// 空一行
<body>
// 空一行
<footer>
```

其中，Header 是必需的，Body 和 Footer 可以省略。

不管是哪一个部分，任何一行都不得超过72个字符（或100个字符）。这是为了避免自动换行影响美观。

Header部分只有一行，包括三个字段：type（必需）、scope（可选）和subject（必需）。

```bash
feat：新功能（feature）
fix：修补bug
docs：文档（documentation）
style： 格式（不影响代码运行的变动）
refactor：重构（即不是新增功能，也不是修改bug的代码变动）
test：增加测试
chore：构建过程或辅助工具的变动

```

### 生成 Change log

生成的文档包括以下三个部分。

```bash
New features
Bug fixes
Breaking changes.
```

conventional-changelog 就是生成 Change log 的工具，运行下面的命令即可。

```bash
npm install -g conventional-changelog
cd my-project
conventional-changelog -p angular -i CHANGELOG.md -w

```

为了方便使用，可以将其写入package.json的scripts字段。

```json
{
  "scripts": {
    "changelog": "conventional-changelog -p angular -i CHANGELOG.md -w -r 0"
  }
}
```

[Commit message 和 Change log 编写指南]
(http://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)

### 修改1

### 修改3

### 修改4

### 修改5