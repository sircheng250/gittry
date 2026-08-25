# Git & GitHub 日常操作手册 (Win7 专用版)

这份操作手册为你梳理了在 Windows 7 下使用 Git 和 GitHub 提交代码的日常标准流程，建议直接保存为项目根目录下的 `README.md` 文件。

---

## 一、 日常修改与提交代码（三步曲）

在你对项目文件进行了修改、新增或删除后，在项目文件夹下右键打开 **Git Bash Here**，依次执行：

### 1. 添加改动到暂存区
```bash
git add .
```

### 2. 提交到本地仓库并添加备注
```bash
git commit -m "本次修改的说明或功能描述"
```
> **⚠️ 注意**：`git add` 和 `git commit` 必须分两行或分两次独立执行，不能连在一起写。

### 3. 推送到远程 GitHub 仓库
```bash
git push
```

---

## 二、 新项目初始化与关联（仅需操作一次）

如果是新创建一个本地项目并推送到 GitHub，请在项目根目录下依次执行：

### 1. 初始化仓库
```bash
git init
```

### 2. 将远程仓库关联为 SSH 地址
*(注：使用 SSH 可以完美避开 Win7 下的 HTTPS 证书报错及 GitHub 密码/Token 验证问题)*
```bash
git remote add origin git@github.com:你的用户名/仓库名.git
```

### 3. 首次推送并绑定默认分支
```bash
git push -u origin main
```
*(注：如果你的默认分支叫 `master`，请将 `main` 改为 `master`)*

---

## 三、 常用辅助命令

* **查看当前仓库状态**（检查有哪些文件被修改或未提交）：
  ```bash
  git status
  ```
* **拉取远程最新代码**（多人协作或多台电脑同步时，开始写代码前建议先执行）：
  ```bash
  git pull
  ```
* **查看当前的远程仓库地址**：
  ```bash
  git remote -v
  ```
