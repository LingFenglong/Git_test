## Git bash

* ### Git 速成

  * ##### 创建文件

    ```bash
    mkdir test
    cd test
    tough README.md
    ```

    

  ***

  * ##### 基本操作

    ```bash
    git status		// 查看状态
    
    git init		// 初始化git 默认生成master主分支
    
    git add <file>	// 放入上传代码的暂缓存 (cache)
    
    git rm --cached <file>		// 把file文件移除缓存区
    
    git commit -m '附带信息内容'	// 提交	-m 提交信息
    
    git log						// 查看所有产生的 commit 记录
    ```

    

  ***

  * ##### 分支 branch    合并merge

    >A, B俩人都在做同一个项目，但是不同的模块
    >
    >A新建了一个分支叫a， B新建了一个分支叫b
    >A、B做的所有代码改动都各自在各自的分支，互不影响
    >
    >等到俩人都把各自的模块都做完了，最后再统一把分支合并起来。、

    ``` bash
    git branch a		// 创建a分支，分支 a 跟分支 master 是一模一样的内容
    
    git checkout a		// 切换到分支a
    
    git checkout -b a	// 创建并切换到分支a
    
    git branch			// 查看当前分支情况
    
    git merge a			// 合并分支a到master
    
    git branch -d a		// 删除已合并的分支a
    
    git branch -D a		// 强制删除分支a
    ```
    
    
    
    ***
    
  * ##### tag
  
    >我们在客户端开发的时候经常有版本的概念，比如v1.0、v1.1之类的，不同的版本肯定对应不
    >同的代码，所以我一般要给我们的代码加上标签，这样假设v1.1版本出了一个新bug，但是又
    >不晓得v1.0是不是有这个bug，有了标签就可以顺利切换到v1.0的代码，重新打个包测试了。
  
    ```bash
    git tag v1.0		// 设置版本标签v1.0
    
    git checkout V1.0	// 切换版本标签到v1.0
    
    git tag				// 查看tag记录
    ```
  
    

***

* ### 向Github提交代码

  * ##### 用户名和邮箱

    >以上进行了全局配置，当然有些时候我们的某一个项目想要用特定的邮箱，这个时候只需切换到你的项目，把 --global 参数去除，再重新执行一遍就ok了。

    ```bash
    git config -global user.name "LingFenglong"			// 设置用户名
    
    git config -global user.email "2808021998@qq.com"	// 设置邮箱
    ```

    

    ***

  * ##### SSH

    >那么什么是 SSH 呢？ 简单点说，SSH是一种网络协议，用于计算机之间的加密登录。目前
    >是每一台 Linux 电脑的标准配置。而大多数 Git 服务器都会选择使用 SSH 公钥来进行授权，所以想要在 GitHub 提交代码的第一步就是要先添加 SSH key 配置。

    ```bash
    git push origin master		// 把本地代码推到远程 master 分支
    
    git pull origin master 		// 把远程最新的代码更新到本地
    
    git remote -v				// 查看当前项目有哪些远程仓库
    
    git remote rm origin		// 移除 origin 远程仓库
    
    git clone git@github.com:LingFenglong/Git_test.git		// 复制仓库
    ```

    

    ***

  * ##### 生成SSH key

    > 成两个文件 id_rsa 和 id_rsa.pub ，而 id_rsa 是密钥，id_rsa.pub 就是公钥。
    >
    >公钥放在github上

    ```bash
    ssh-keygen -t -rsa
    ```

    

    ***

* ### Git进阶

  * 
