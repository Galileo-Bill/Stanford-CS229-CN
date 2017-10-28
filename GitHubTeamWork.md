**所有内容来自于：https://help.github.com/categories/collaborating-with-issues-and-pull-requests/。  
以下内容已被@AcceptedDoge 进行简单汉化，对应部分英文页面链接已经给出。**

# Fork A Repo
_英文原文来自 GitHub Help [此页面](https://help.github.com/articles/fork-a-repo/)_  
> 一个 Fork 就是一个存储库的副本，使用Fork来分支存储库允许你自由地尝试更改而不影响原始项目。

Fork 最常见的用途是对其他人项目进行改进，或者使用别人的项目作为你自己的想法的起点。  
### 对其他人项目进行改进
使用 Fork 提出更改的一个很好的例子是修复BUG，而不仅是记录你发现错误的 Issue，你可以：  
1. Fork 该存储库。
2. 做出一些修复。
3. 向存储库所有者发起 Pull Request  。

如果存储库所有者喜欢你的工作，他们很有可能把你的修复 Pull 到原始的存储库。  
### 使用别人的项目作为你自己的想法的起点
[开源的核心理念](http://opensource.org/about)是通过共享代码，使得我们可以做出更好，更可靠的软件。从某人的项目的分支中创建公用存储库时，请确保包含一个[许可证文件](http://choosealicense.com/)，以确定你希望将项目与他人共享的方式。有关开放源代码的更多信息，例如具体如何创建和扩展开放源码项目，我们创建了[开源代码指南](https://opensource.guide/)，将通过为你的开源项目创建和维护存储库提供最佳实践来帮助你培养一个健康的开源社区。

## 使用举例
分支存储库是一个简单的两步过程。我们创建了一个存储库，供你练习！  
1. 在GitHub上，导航到 [octocat / Spoon-Knife](https://github.com/octocat/Spoon-Knife) 存储库。
2. 在页面的右上角点击Fork。

就是这么简单！现在你有了一个原来的 octocat / Spoon-Knife 仓库的 Fork。

## 保持你的 Fork 同步
你可能会分支一个项目，以便向 _上游（upstream）_ 或 _原始（original）_ 存储库提出更改。在这种情况下，一个很好的做法是定期将你的分支与上游资源库进行同步。为此，你需要在命令行中使用 Git 。你可以使用相同的 [octocat / Spoon-Knife](https://github.com/octocat/Spoon-Knife) 仓库练习设置上游存储库！

### 步骤1：设置Git
如果还没有，你应该首先[设置Git](https://help.github.com/articles/set-up-git)。不要忘了[从Git设置GitHub的身份验证](https://help.github.com/articles/set-up-git#next-steps-authenticating-with-github-from-git)。

### 步骤2：创建Fork的本地克隆
现在，你有一个Spoon-Knife存储库的Fork，但你的计算机上没有该存储库中的文件。让我们在你的计算机上创建你的Fork的 _克隆（Clone）_ 。
1. 在GitHub上，导航到**你的**Fork仓库。
2. 在存储库名称下，单击**克隆**或**下载**（Clone or download）。
3. 在“克隆HTTP”（Clone with HTTPs）部分中，单击  复制存储库的克隆URL（ to copy the clone URL for the repository）。
4. 打开Git Bash。
5. 键入`git clone`，然后粘贴你在步骤2中复制的URL。它将如下所示，注意使用你的GitHub用户名，而不是`YOUR-USERNAME`：
```
$ git clone https://github.com/YOUR-USERNAME/Spoon-Knife
```
6. 按**回车**。您的本地克隆将被创建。
```
git clone https://github.com/YOUR-USERNAME/Spoon-Knife
Cloning into `Spoon-Knife`...
remote: Counting objects: 10, done.
remote: Compressing objects: 100% (8/8), done.
remove: Total 10 (delta 1), reused 10 (delta 1)
Unpacking objects: 100% (10/10), done.
```
现在你就有了一个你的Fork存储库的本地副本啦！

### 步骤3：配置Git将你的Fork与原始的Spoon-Knife仓库同步
1. 在GitHub上，导航到**你的**Fork仓库。
2. 在存储库名称下，单击**克隆**或**下载**（Clone or download）。
3. 在“克隆HTTP”（Clone with HTTPs）部分中，单击  复制存储库的克隆URL（ to copy the clone URL for the repository）。
4. 打开Git Bash。
5. 将目录更改为你在步骤2中克隆的Fork的位置。
> 要转到你的主目录，只需键入`cd`即可，无需别的内容。
> 要列出当前目录中的文件和文件夹，请键入`ls`。
> 要进入你·列出的其中一个目录，请键入`cd your_listed_directory`。
> 要进入上一级目录，请键入`cd ..`。
6. 键入`git remote -v`并按**Enter**键。你将看到你的Fork的当前配置的远程存储库。
```
$ git remote -v 
origin https://github.com/ YOUR_USERNAME / YOUR_FORK .git（fetch）
origin https://github.com/ YOUR_USERNAME / YOUR_FORK .git（push）
```
7. 键入`git remote add upstream`，然后粘贴您在步骤2中复制的URL，然后按Enter键。它将如下所示：
```
$ git remote add upstream https://github.com/octocat/Spoon-Knife.git
```
8. 要验证你为Fork指定的新上游存储库，请再次键入`git remote -v`。您应该看到您的叉`origin`的URL和原始存储库的URL `upstream`。
```
git remote -v
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (fetch)
origin    https://github.com/YOUR_USERNAME/YOUR_FORK.git (push)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (fetch)
upstream  https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY.git (push)
```
现在，你可以使用几个Git命令使您的Fork与上游存储库同步。有关详细信息，请参阅“[Syncing a fork](https://help.github.com/articles/syncing-a-fork)”。

## 下一步
你可以对你的 Fork 进行天马行空的修改，包括：
- **创建分支**： [分支（Branches）](https://help.github.com/articles/creating-and-deleting-branches-within-your-repository/)允许你构建新功能或测试创意，而不会使你的主要项目面临风险。
- **发起 pull requests**： 如果你希望回馈到原始存储库，您可以向原始作者发送请求，通过提交拉取请求将Fork拉入其存储库。

# Syncing a fork
_英文原文来自 GitHub Help [此页面](https://help.github.com/articles/syncing-a-fork/)_  
> 同步存储库的一个Fork，使其与上游存储库保持最新。

在将fork与上游存储库同步之前，必须[配置指向 Git 上游存储库的远程](https://help.github.com/articles/configuring-a-remote-for-a-fork)。（柴犬注：在上面的教程里面已经有相关操作说明）

1. 打开Git Bash。
2. 将当前工作目录更改为本地项目。
3. 从上游存储库获取分支及其各自的提交。`master`的`commit`将存储在本地的`upstream/master`分支机构中。
```
$ git fetch upstream
remote: Counting objects: 75, done.
remote: Compressing objects: 100% (53/53), done.
remote: Total 62 (delta 27), reused 44 (delta 9)
Unpacking objects: 100% (62/62), done.
From https://github.com/ORIGINAL_OWNER/ORIGINAL_REPOSITORY
 * [new branch]      master     -> upstream/master
```
4. 切换（checkout）到你的Fork的本地`master`分支。
```
$ git checkout master
Switched to branch 'master'
```
5. 将`upstream/master`的更改合并（Merge）到本地`master`分支中。这将使你的`master`分支机构与上游存储库同步，而不会丢失本地更改。
```
$ git merge upstream/master
Updating a422352..5fdff0f
Fast-forward
 README                    |    9 -------
 README.md                 |    7 ++++++
 2 files changed, 7 insertions(+), 9 deletions(-)
 delete mode 100644 README
 create mode 100644 README.md
```
如果你的本地分支没有任何唯一的提交，Git将改为执行“快进（fast-forward）”：
```
$ git merge upstream/master
Updating 34e91da..16c56ad
Fast-forward
 README.md                 |    5 +++--
 1 file changed, 3 insertions(+), 2 deletions(-)
```

# Pushing to a remote
_英文原文来自 GitHub Help [此页面](https://help.github.com/articles/pushing-to-a-remote/)_  

使用`git push`推送你的本地分支的commits到远程仓库。
`git push`命令有两个参数：
- 远程名称，例如， origin
- 一个分支名称，例如， master

例如：
```
$ git push <REMOTENAME> <BRANCHNAME>
```
我们通常`git push origin master`会将本地更改推送到在线存储库。

## 重命名分支
要重新命名一个分支，您可以使用相同的git push命令，但是您还可以添加一个参数：新分支的名称。例如：
```
$ git push  <REMOTENAME> <LOCALBRANCHNAME>:<REMOTEBRANCHNAME> 
```
这推送`LOCALBRANCHNAME`分支到你的`REMOTENAME`远程，但它被重命名为`REMOTEBRANCHNAME`。

## 处理“非快进”错误
如果你的存储库的本地副本与你要推送的上游存储库不同步或“落后（behind）”，您会收到一条消息`non-fast-forward updates were rejected`。这意味着在您能够推送本地更改之前，您必须检索或“提取（pull）”上游更改。
有关此错误的更多信息，请参阅“ [处理非快速错误](https://help.github.com/articles/dealing-with-non-fast-forward-errors)”。

## 推送标签
默认情况下，没有其他参数，git push将发送与远程分支具有相同名称的所有匹配分支。  
要推送单个标签，您可以发出与推动分支相同的命令：
```
$ git push <REMOTENAME> <TAGNAME>
```
要推送所有标签，您可以键入命令：
```
$ git push <REMOTENAME> --tags
```
## 删除远程分支或标签
删除分支的语法乍一看是有点神秘的：
```
$ git push <REMOTENAME> ：<BRANCHNAME>
```
请注意，冒号前面有一个空格。该命令类似于您重命名分支所需的相同步骤。然而，在这里，你告诉Git的推送nothing到`REMOTENAME`的`BRANCHNAME`分支。因此，`git push`将会删除远程存储库上的分支。

# Creating a pull request from a fork
_英文原文来自 GitHub Help [此页面](https://help.github.com/articles/creating-a-pull-request-from-a-fork/)_  

> 如果你已经分支了存储库并对fork进行了更改，可以通过创建一个拉取请求（pull request） 来询问上游存储库是否接受你的更改。

你可以从任何分支打开上游存储库的 pull request，或在Fork中提交。我们建议你在主题分支中进行更改，以便你可以在你的拉取请求收到反馈后推送跟进提交。你还可以选择使上游存储库的维护者能够在你的主题分支上提交对你的pull request的更新。如果你的pull request将你的主题分支与上游存储库中的分支作为基本分支进行比较，那么你的主题分支也称为pull request的compare分支。有关拉取请求分支（包括示例）的更多信息，请参阅“ [Creating a Pull Request](https://help.github.com/articles/creating-a-pull-request/#changing-the-branch-range-and-destination-repository)”。

1. 导航到你创建Fork的原始存储库。
2. 在分支菜单右侧，单击**New pull request**。
![pull-request-start-review-button](https://help.github.com/assets/images/help/pull_requests/pull-request-start-review-button.png)
3. 在“比较”页面上，单击**compare across forks**。
![compare-across-forks-link](https://help.github.com/assets/images/help/pull_requests/compare-across-forks-link.png)
4. 确认base fork是你要用来合并更改到的目的存储库。使用base branch 下拉菜单选择要将更改合并到的上游存储库的分支。
![choose-base-fork-and-branch](https://help.github.com/assets/images/help/pull_requests/choose-base-fork-and-branch.png)
5. 使用 head fork下拉菜单选择你的fork，然后使用compare branch下拉菜单选择你进行更改的分支。
![choose-head-fork-compare-branch](https://help.github.com/assets/images/help/pull_requests/choose-head-fork-compare-branch.png)

```
base branch：相当于target branch，你希望Pull Request被merge到上游项目的哪个branch里。
为什么要叫base branch：base可以理解为你在进行git rebase操作时的那个“base”，也就是你的主题branch所基于的开发base（基础）。

head branch：相当于source branch，你希望自己开发库里的哪个branch被用来进行Pull Request（当然也就是你的主题branch）。
为什么要叫head branch：参见下面关于head的定义。

注意head与HEAD（大写）的区别：

head：简单地理解，就是指向某个commit对象的一个reference。它可以是一个branch的名称（例如，默认的master），也可以是一个tag的名称。一个库可以同时有任意多个head。
HEAD：当前活动的head。在任意时刻，存在且仅存在一个HEAD。它可以是指向当前branch的head（比如，指向master，假如master是当前branch的话）；也可以不指向任何特定的branch（这叫做detached HEAD）。
系统会从你选择的head branch（在这里，是主题branch）的这个head开始匹配所有不包含在base branch中的commits，然后自动视作你的主题branch相对于base所增加的新特性，放进同一个Pull Request中提交。
```
6. 输入您的拉动请求的标题和说明。
7. 如果您不希望允许有权访问上游存储库的任何人更改您的PR，请取消选择“ **Allow edits from maintainers**”。
8. 单击**Create pull request**。
