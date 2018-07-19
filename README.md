# git学习
远程仓库：

    1、git 添加远程github仓库的时候提示错误：fatal: remote origin already exists. 

        先删除远程 Git 仓库 git remote rm origin

        再添加远程 Git 仓库 git remote add origin git@github.com:tianxinli/learngit.git

    2、想把代码提交到Git上 

    fatal: Could not read from remote repository.（无法从远程存储库读取）

    Please make sure you have the correct access rights and the repository exists.

    问题原因： 在git上没有创建SSH Key
    
    1、在终端中输入

    ssh-keygen -t rsa -C "username" (注：username为你git上的用户名)

    三次回车，如有看到The key's randomart image is，代表你的SSH Key生成成功了。

    cat ~/.ssh/id_rsa.pub

分支管理:

    1、查看分支：git branch

    2、创建分支：git branch <name>

    3、切换分支：git checkout <name>

    4、创建+切换分支：git checkout -b <name>

    5、合并某分支到当前分支：git merge <name>

    6、删除分支：git branch -d <name>

    7、如果要丢弃一个没有被合并过的分支，可以通过git branch -D <name>强行删除。

    8、Git还提供了一个stash功能，可以把当前工作现场“储藏”起来 git stash

    9、刚才的工作现场存到哪去了？用git stash list命令看看

    10、工作现场还在，Git把stash内容存在某个地方了，但是需要恢复一下

    一是用 git stash apply 恢复，但是恢复后，stash内容并不删除

    另一种方式是用 git stash pop，恢复的同时把stash内容也删了

    先用git stash list查看，然后恢复指定的stash，用命令：git stash apply stash@{0}
