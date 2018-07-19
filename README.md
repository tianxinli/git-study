# git学习

## 分支:
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
