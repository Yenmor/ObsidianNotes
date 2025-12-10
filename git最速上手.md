---


- # 配置git身份

```bash
git config --global user.name "用户名"
git config --global user.email "邮箱"
```

- # 初始化本地 Git 仓库

```bash
git init
```

- # 将项目文件添加到暂存区

```bash
git add .
```

" . " 会将当前目录下所有文件添加到暂存区， 也可以替换成文件名

- # 提交本地文件到仓库

```bash
git commit -m "提交信息"
```

- # 关联远程仓库

```bash
git remote add origin <远程仓库URL>
```

例： `git remote add origin https://github.com/Yenmor/ActionWatcher4j.git`
- # 修改本地分支命名

```bash
git branch -M main
```

- # 推送到远程仓库

```bash
git push -u origin main
```



