# CoC-Replay

## Update

### 人物素材

- 暂缺：平冈、小早川
- 替换：手持物和乔装
  - 怎么继承头发的蒙皮啊……实在不行放弃头发算了，反正也不太看得出来
  - 乔装还得拆小人，我恨

### 动作拆分

- 标准动作

  单人常见动作置于`Animation/name/`文件夹中。

  - 眨眼
  - 说话
  - 走路：鸟居的走路动作较为女性化，待调整。
  - 幕后吐槽

- 剧本动作按幕存放，当前进度`A3S1`

### 一些问题

- **流汗动作bug，骨头不见了QAQ**
- **脸庞，估计是边缘半透明度的问题，我选择狗带**

## Help

Unity repo for CoC replay
简单解释一下Git的使用。

### 初始化

首先找到一个文件夹，打开terminal，输入：

```
git clone https://github.com/Josep-h/CoC-Replay.git
```

第一次下载需要时间较长，因为Library比较大……后面应该就好了。

### 设置全局GitHub帐号信息

```
git config --global user.name 'runoob'
git config --global user.email test@runoob.com
```

### 开始修改前

在开始修改前请习惯性来一次：

```
git pull
```

以保证现在的文件和remote版本一致。

### 分支

分支是为现在的master（或者另一个分支）创建一个副本，对于这个副本的修改会保留在这个副本中，修改结束可以将副本和master合并来保留修改。这个功能可以便于处理需要重要的功能增加或者迭代的时候。

- 如果需要暂时测试一个新功能或者长时间开发一个新内容，请先使用（如果是小幅度修改可以不用 branch ）：`git branch (name)`
    e.g. : `git branch characters`

- 查看所有分支：`git branch`。

- 切换分支：`git checkout (name)`。

- 合并（name）分支到当前分支：`git merge (name)`。在合并前请先**commit**。

- 删除分支：`git branch -d (name)`。

### 提交

需要先将缓存的信息放到代码中。（在 merge 之前也需要）

- 在git中添加修改文件：`git add .`
- 查看当前修改文件：`git status -s`：这个指令可以看到所有本次修改的文件。如果在文件前标注为AM（红色标识），则需要再一次使用`git add .`将缓存信息存入。
- 提交文件：`git commit -m "blabla..."`

最后提交文件（如果有branch，需要先合并branch）

```
git push
```

如果出现冲突…嗯，这个好像几句话说不清楚，就先不管它。


### 参考修改流程：

```
git pull
git branch newbranch
git checkout newbranch
# after modified
git add .
git commit -m "XXX is added..."
git checkout master
git merge newbranch
git push
git branch -d newbranch
```

**简化流程**

这个流程不涉及 branch 操作：

```
git pull
# after modified
git add .
git commit -m "XXX is added..."
git push
```

为了真正的懒人，写了俩简洁更新脚本。在更新前运行`init.cmd`，修改结束后运行`update.cmd`。效果和上述简化流程相同。

### 参考：

[Git 分支管理](https://www.runoob.com/git/git-branch.html)

[Git 基本操作](https://www.runoob.com/git/git-basic-operations.html)

如果觉得上述的操作很难受，可以使用Visual Studio Code。其中带有完整的GUI GitHub管理工具，也很简单。请参见[这个链接](https://zhuanlan.zhihu.com/p/31417255)

祝好。



