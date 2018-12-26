### git 命令

##### git status

> 查看文件当前的状态


##### git add

> 修改文件 已修改、新添加的文件状态从为跟踪变为以跟踪
> 在修改文件或者现价文件后必须使用 git add 修改文件状态 ，否则不能成功提交




##### 关于.gitignore 文件

> 用户配置不需要提交到git上的文件、目录
> 使用语法：
>> # 注释
>> *  glob模式、统配符  例如：*.a 会忽略所有.a文件扩展名文件
>> /todo 忽略/todo目录下所有文件 ** 只有这个目录下 **
>> todo/ 忽略todo/所有文件
>> todo/*.txt 忽略todo目录下所有.txt文件 （不包括 todo/server/*.txt）
>> todo/**/*.txt 忽略todo目录下所有.txt文件
