####################################
----
#Beyond Compare作为git的比对与合并工具
---
##Windows下使用Beyond Compare作为git的比对与合并工具：
###介绍：
新手对于git的bash命令不太熟悉，可能比较习惯用图形化工具，这里就介绍一种文件比对工具：Beyond Compare

----
###操作：
在系统目录下，这里是：C:\Users\Ucar，可以看到一个配置文件：.getconfig,
使用notepad++编辑器来修改，这里要改以下几行内容：
>     #difftool 配置 :
>     [difftool "bc4"]
>         cmd = "\"c:/program files/beyond compare 4/bcomp.exe\" \"$LOCAL\" \"$REMOTE\""


>     #mergeftool 配置:   
>     [mergetool "bc4"]
>         cmd = "\"c:/program files/beyond compare 4/bcomp.exe\" \"$LOCAL\" \"$REMOTE\" \"$BASE\" \"$MERGED\""
>     

这里要对照自己的compare安装目录，来对应的填充
然后git命令行中执行相关命令就ok啦：）
>     #比对当前文件相对于Head版本的改动
>     git difftool <file_name>
>     #当merge <branch_name>提示冲突时，执行下面命令便可以调出bc合并冲突
>     git mergetool
然后在compare软件中继续修改就可以了。。。

---------------------

