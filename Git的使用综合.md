***
## Git 环境设置


-  ### Git 提供以下控制级别
>- local
> - global
> - System


- ###  local 本地配置

> 作为文件存储在 `.git/config`


- ### global 全局配置

>存储在 `C:\Users\XXX\.gitconfig`

- ### System 系统配置

>存储在 `C:ProgramData\Git\config`

***

## Git 配置命令

- 列出git所有命令
```bash
git config --list
```

<br>

- 设置当前用户每次提交使用的用户名和电子邮件
```bash
git config --global user.name "Name"
```
```bash
git config --global user.emal "xxx@xx.xx"
```

***

## Git 术语
>**Repository** 存储库，包含文件的集合以及对这些文件所做的更改历史记录。
>
>**Branch** 分支是与主要工作项目不同的存储库版本。
>
>**Clone** 用于制作目标存储库的副本或克隆它。
>
>**Fetch** 用于从存储库中获取分支和标签。
>
>**Master** 它是 Git 的默认分支。
>
>**Origin** 对最初克隆的项目的远程存储库的引用。
>
>**Pull** 获取远程服务器上的更改并将其合并到您的工作目录中。
>
>**Push** 将本地存储库内容上传到远程存储库。

***

## Git 命令
```bash

# 配置相关命令
git config    # 用途：设置Git配置信息（用户名、邮箱、编辑器等）
git init      # 用途：初始化新的Git仓库，创建.git目录

# 仓库操作命令
git clone     # 用途：克隆远程仓库到本地，创建完整副本
git status    # 用途：显示工作目录和暂存区的状态

# 文件跟踪命令
git add       # 用途：将文件添加到暂存区，准备提交
git rm        # 用途：从工作区和暂存区删除文件

# 提交历史命令
git commit    # 用途：将暂存区的更改提交到版本历史
git log       # 用途：显示提交历史记录
git reset     # 用途：重置当前HEAD到指定状态（可回退版本）

# 分支操作命令
git branch    # 用途：创建、列出、删除分支
git merge     # 用途：合并指定分支到当前分支

# 远程协作命令
git push      # 用途：将本地提交推送到远程仓库
git pull      # 用途：从远程仓库获取并合并更改（fetch + merge）

# 临时存储命令
git stash     # 用途：临时保存工作目录的修改，便于切换分支
git revert    # 用途：创建新的提交来撤销指定提交的更改
```