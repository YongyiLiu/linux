# linux
linux的学习笔记

 "#:超级管理员   $：普通用户"

--all  equ  -a   ;  -a -l  equ -al

命令格式：

    comand [选项] [参数]  <----> ls -l /etc     (参数：指的是操作的对象，若无参数，则默认是操作当前的位置)

-rw-r--r--:

  解析：第一个“-”表示文件类型(- 文件； d目录；l软链接文件)
  
        u代表所有者  g代表所属组 o代表其他人
        
        r读 w写 x执行
        
文件处理：

    mkdir -p  递归创建   如：mkdir -p Yongyi/zucker
    
    rm 删除    mv 移动   cp 复制(复制目录：cp -r )
    
    显示当前路径: pwd   切换到home目录： cd or cd ~   切换到上一个工作目录： cd -    更改当前工作路径为path: $cd path
    
    查找目录及文件 find/locate     如：find ./ -name "yongyi"
    
    查看文件：cat vi head tail more
    
    改变文件的拥有者 chown
    
管道和重定向：

    批处理命令连接执行，使用 |
    
    串联: 使用分号 ;
    
    前面成功，则执行后面一条，否则，不执行:&&
    
    前面失败，则后一条执行: ||
    
文本处理工具：

磁盘管理：

  查看磁盘空间利用大小: df -h
  
  查看目录大小 du -sh
  
  打包/压缩 ： 
  
      打包(多个文件合并为一个文件)：tar -cvf etc.tar  
      
        -c :打包选项
        
        -v :显示打包进度
        
        -f :使用档案文件
        
      解包 tar -xvf 
      
      压缩 $gzip demo.txt 
      
      解压缩 gunzip bzip
      
进程管理工具：

  查看进程：$ps -ef
  
  终止进程：$kill PID
  
  进程监控（使用CPU、使用内存最多的进程）：$top
  
  分析线程栈：pmap PID
  
性能监控：

  查看CPU使用率：sar -u
  
  查询内存：free -m
  
  查看工具： 查看cpu、内存、使用情况： vmstat n m （n 为监控频率、m为监控次数）
  
网络工具：

  查询网络服务和端口：netstat
  
  网络路由：$route -n
  
  DNS查询：host domain
  
  反向DNS查询: $host IP
  
系统管理：

  查看Linux系统版本:$lsb_release -a


