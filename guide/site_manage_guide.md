# 网站文章发布与维护指南

## 准备工作

> 我们推荐使用的编辑器是Visual Studio Code，本文基于[Visual Studio Code](https://code.visualstudio.com/)讲解。我的设备是Macbook Pro，因此以下讲解基于macOS和Mac版的VS Code编写，可能会有些许出入，细节问题请通过[Google](https://www.google.com/)或其他搜索引擎搜索解决或直接询问我。

- 准备一个GitHub账户。如果您没有GitHub账户，请先注册一个。

    然后提供您的账号给Bill-Haku，让他将您的账号添加到代码仓库的Collaborator中。

- 安装Git

    如果您使用的是Windows，则需要在您的电脑上安装Git，并且需要在Visual Studio Code中安装Git Extension。您可以在[Git](https://git-scm.com/)中找到安装方法。安装好后，您可以在Visual Studio Code中打开Git Extension，并且在Git Extension终端中输入`git config --global user.name "Your Name"`，然后再输入`git config --global user.email "Your Email"`。

    如果您使用的是macOS或Linux，则Git已经被预装在系统中，可以直接在Visual Studio Code中打开Git Extension。如果您没有使用过，您同样需要配置您的用户名和邮箱。

    **当然，您也不一定一定要使用shell命令完成配置。VSCode中似乎有图形化的直接配置Git信息的方式。**

- 克隆仓库

    打开VSCode后，您可以在Get Started页面找到`Clone Git Repository`，然后输入本站的代码地址`https://github.com/Bill-Haku/Bill-Haku.github.io.git`，按照指引完成操作。

    克隆完成后，在您选择保存文件的地方将会有本站的完整源代码，您可以直接在VSCode中打开这个文件夹。

## 发布文章

1. 将新文章放到`_posts`文件夹中。

    如果您的文章是在`_drafts`文件夹中，那么您需要将其移动到`_posts`文件夹中。

    关于文章的标题的格式和内容的格式，请参考目录下的`post_sample.md`文件。

2. 将仓库提交到Github仓库。

    在VS Code的左侧您可以看到一个`Source Control`的图标，点击这个图标，然后在`Changes`右侧点击`+`将所有修改了的文件添加到`Staged Changed`中。然后在上方的文本框中输入commit信息，即关于本次commit的说明。然后点击`Commit`按钮，完成提交。然后在`Source Control`的右侧`...`中点击`Push`，完成上传到Github仓库。

## 关于图片和其他静态资源

图片可以放在`img`文件夹中。此外建议对每篇文章新建一个文件夹便于图片的管理，每篇文章的标题头图命名为`title.jpg/png`，其他图片按照使用顺序编号。当然，文件名也可以按照文件的内容或用途命名。然后在需要使用的地方使用`http://zhuaiyuwen.xyz/img/.../img.png`这样的链接即可。

静态资源同理，如用于公共分发的文件可以放在`share`文件夹中，然后使用`http://zhuaiyuwen.xyz/share/file.zip`这样的链接即可让用户访问并下载。

---

在上传完成后，Github Action将会自动开始根据新内容构建网站，并且自动更新。整个过程的持续时间一般不会超过10分钟，通常在2分钟左右完成。完成后，刷新之外语文网站页面，您就可以看到新发布的文章
