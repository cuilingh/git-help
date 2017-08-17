# git-help
初次配置Git


Windows:


下载安装Git

在浏览器地址栏上输入10.1.130.212，创建GitHub帐号。
点击New Project，需要输入Project name ，即你要做的项目名称，尽量简短点。
生成ssh key：右键空白处，选择Git BASH Here。输入ssh-keygen，一直回车到结束。
打开：用'cat'命令打开id_rsa.pub，默认地址在~/.ssh/id_rsa.pub

在GitLab页面，点击右上角圆形头像，选择settings，选择SSH Keys，在key中粘贴刚才复制的内容，在title里注明这是你哪台机子的。选择add key。
在终端配置Git的配置文件：

git config --global user.name "your name"      //配置用户名
git config --global user.email "your email"    //配置email

或者进入自己建立的project，分别复制两个'git global setup'的命令，在Git GUI粘贴输入回车



Linux:


安装git: 使用命令sudo apt-get install git

在浏览器地址栏上输入10.1.130.212，创建GitHub帐号。
点击New Project，需要输入Project name ，即你要做的项目名称，尽量简短点。
生成ssh key:在终端使用命令'ssh-keygen'，一直回车到结束
打开ssh key:位置：~/.ssh/id_rsa.pub用cat命令打开，即cat id_rsa.pub

在GitLab页面，点击右上角圆形头像，选择settings，选择SSH Keys，在key中粘贴刚才复制的内容，在title里注明这是你哪台机子的。选择add key。
在终端配置Git的配置文件：

git config --global user.name "your name"     //配置用户名
git config --global user.email "your email"   //配置email





第一次上传


设定一个文件夹目录为上传文件的目录，打开到目录后，使用命令git init，Win版是在上传文件的目录下，右键空白处，选择Git BASH Here，然后输入命git init。
创建本地仓库：使用命令git remote add origin git@10.1.130.212:yourName/yourRepo.git
youname是你的GitHub的用户名，yourRepo是你要上传到GitHub的仓库，这是你在GitHub上添加的仓库。可以在你的project里找到这个命令。
添加README：

touch README.md
git add README.md
git commit -m 'add README'
git push -u origin master


添加文件：添加一个文件xxx到本地仓库，使用命令git add xxx，可以使用git add .自动判断添加哪些文件
说明提交：使用命令git commit -m '这次的提交的说明(如更改了哪些内容)'

提交到远程仓库：使用命令git push origin master，有时候出错，是因为远程仓库在其他地方更新了，本地的没更新，在提交前使用命令git pull origin master更新下本地的仓库



之后再上传只要后面三步就行了



从GitHub克隆项目到本地

选择要存放的目录后，使用命令 git clone https://github.com/***/***.git
