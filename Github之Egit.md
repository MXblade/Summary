#Github之egit
##egit
###egit是eclipse上的github的插件，能够管理github上的项目，但操作不如github for windows方便。
###使用：
Eclipse Mars版本已经内置了egit。
####将已有的普通项目部署到github
#####1.项目转化成git仓库
目标项目右键->Team->Shared project
![](http://i.imgur.com/uxtjrx2.png)
选上Use or create repository in parent folder of project,将该项目转化为git仓库。![](http://i.imgur.com/ON9b4Qv.png)
选择Create Repository->finish。完成git仓库的转化
#####2.将git仓库部署到github
git仓库右键->Team->Commit
![](http://i.imgur.com/ElABjTD.png)
在commit message中填写更新内容
选中下面需要更新的文件，之后可以选择commit更新本地仓库，或者选择commit and push更新仓库并push到github上，完成github的项目更新。
#####3.push操作
git仓库右键->Team->Remote->Push
![](http://i.imgur.com/ia6emMA.png)
URI:填写github上对应仓库的链接，需要已经存在。下面的两项会自动填写。
User和Password就是对应的github的用户名和密码
![](http://i.imgur.com/5c6x2s0.png)
source ref 选择master,再选择Add Spec，
下面Specifications for push中，选择force update
finish就可完成项目的部署。

####将github上的项目clone到eclispe
import->Git->Projects from Gie->Clone URI->填写对应的仓库在github的位置和用户信息，选中需要clone的内容，next->填写存储本地位置->选择对应的项目(已存在或通常项目)->项目名称->Finish



###PS
####eclipse的项目转化成git仓库后，将项目中的.git文件夹删除后，就变成了原先的项目。
####从github上clone项目非常缓慢，若项目很大，经常出错无法clone，还未尝试解决方案。
####从github上将项目打包下载很快，但得到的不是git仓库，而是一个普通的项目文件。