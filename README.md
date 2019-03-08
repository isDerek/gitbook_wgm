![wpiLogo](images/wpiLogo.jpg)
# 1.文档维护说明

##基本流程

```
## 克隆仓库
git clone git@github.com:isDerek/gitbook_wgm.git

# 若提醒你并没有绑定远程仓库（公钥已提交给仓库管理员），请执行提示命令：
git remote add origin git@github.com:isDerek/gitbook_wgm.git
```

```
## 克隆本地后，修改重新提交到仓库即可（已完成绑定远程仓库步骤）

git status // 查看仓库文件所做修改
git add .  // 添加修改文件到本地的临时仓库
git commit -m "你所做的修改注释"  // 添加文件到本地仓库
git push   // 提交本地仓库到远程仓库

# git push 若告诉你还没有绑定远程仓库分支，此时敲击以下命令
git push --set-upstream origin master
```

**notes: <br>**
**注意若是第一次使用 git ，git 的安装不做说明，不断下一步即可，安装好后，执行以下命令**

I. 创建本地 git 个人信息

```
git config --global 你的用户名
git config --global 你的邮箱（已在 github 官网注册了的邮箱，请去 github 官网申请个人账户）
```
II. 生成私钥和公钥（用于绑定远程仓库）

```
# 生成私钥和公钥

# 查看是否有生成过私钥和公钥，若存在 id_dsa（私钥）和 id_dsa.pub（公钥）,则忽略生成公私钥步骤

cd ~/.ssh // Linux \ Mac 系统环境下 git 公私钥存放路径

# Windows 则包含在 C:/User/自己的用户名/.ssh 中

# 1. 若公私钥不存在，则执行以下命令,过程中不断回车即可

ssh-keygen -t rsa -C "你的邮箱地址"

# 2. 将公钥告诉 github 仓库的管理者，请他将你的公钥添加进仓库，至此完成允许访问远程仓库

```

##文档的目录结构

```
|—— README.md               # 文档说明
|—— SUMMARY.md              # 目录
|—— _book                   # gitbook 配置文件目录
|—— ProjectIntro.md         # 项目概述
|—— ProtocolIntroduce.md    # 协议概述
|—— MeetingMinutes.md       # 无线电竞鼠标会议记录
|—— device.md               # 设备端概述
|—— book.pdf                # gitbook 构建的 PDF 文件
|—— images                  # 放置文档中使用的图片
|—— device                  # 设备层文档目录
|—— Protocol                # 协议层文档目录
|—— graph                   # 放置各种流程图
```
