### git 命令

##### git status

> 查看文件当前的状态


##### git add

> 修改文件 已修改、新添加的文件状态从为跟踪变为以跟踪
> 在修改文件或者现价文件后必须使用 git add 修改文件状态 ，否则不能成功提交

##### git diff
> 查看尚未暂存的文件更新了那些内容

##### git diff --cached  git diff --staged
>  查看暂存区更新了那些内容


##### git commit 
 > 提交更新 将add 后的暂存区 添加的提交记录
 
 
##### git commit -a （跳过 git add）
> 因为每次提交前都需要先add 比较麻烦，所有可以使用 git commit -a 来解决，git会自动把所有已跟踪过的文件暂存起来一并提交。从而跳过 git add 步骤

##### git rm (会移除文件)
> 要从git 中移除某个文件，就必须从已跟踪文件清单中移除，并且会删除目录中的文件。
> 如果删除之前已经放到了暂存区，必须使用 git rm -f 强制删除
> 可以使用 正则进行匹配删除 git rm log/\*.log (正则斜杠转义)

##### git rm --cached (从暂存区中删除记录)
> 出现错误暂存记录时，需要是使用 git rm --cached 来删除暂存区记录，这样可以保留，目录下文件 

##### 我在线上修改了 readme.md 的文件

##### 关于.gitignore 文件

> 用户配置不需要提交到git上的文件、目录
> 使用语法：
 * #号  注释
 *  glob模式、统配符  例如：*.a 会忽略所有.a文件扩展名文件
 * /todo 忽略/todo目录下所有文件 ** 只有这个目录下 **
 * todo/ 忽略todo/所有文件
 * todo/*.txt 忽略todo目录下所有.txt文件 （不包括 todo/server/*.txt）
 * todo/**/*.txt 忽略todo目录下所有.txt文件	
