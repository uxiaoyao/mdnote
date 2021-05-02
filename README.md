# gitbook 安装&搭建

![](https://raw.github.com/GitbookIO/gitbook/master/preview.png)
[npm 库](https://www.npmjs.com/package/gitbook)

[![](https://gblobscdn.gitbook.com/spaces%2Fgitbook%2Favatar-rectangle.png?alt=media)](https://docs.gitbook.com/)  
  
  
GitBook can be installed from NPM using:

    $ npm install gitbook-cli -g
Create the directories and files for a book from its SUMMARY.md file (if existing) using

    $ gitbook init
You can serve a repository as a book using:

    $ gitbook serve
Or simply build the static website using:

    $ gitbook build

1、nohup   
#### 将程序以忽略挂起信号的方式运行起来

>补充说明
nohup命令 可以将程序以忽略挂起信号的方式运行起来，被运行的程序的输出信息将不会显示到终端。
无论是否将 nohup 命令的输出重定向到终端，输出都将附加到当前目录的 nohup.out 文件中。
如果当前目录的 nohup.out 文件不可写，输出重定向到$HOME/nohup.out文件中。
如果没有文件能创建或打开以用于追加，那么 command 参数指定的命令不可调用。
如果标准错误是一个终端，那么把指定的命令写给标准错误的所有输出作为标准输出重定向到相同的文件描述符。
简单实例：  
     
    nohup command &

指定输出实例  
    
    nohup command > myout.file 2>&1 &


#### 其他相关命令
>ctrl + z #可以将一个正在前台执行的命令放到后台，并且处于暂停状态。
fg #将后台任务切换到前台执行
bg #将一个在后台暂停的命令，变成在后台继续执行。如果后台中有多个命令，可以用bg %jobnumber将选中的命令调出
jobs #查看后台运行的状态，jobs -l选项可显示所有任务的PID
ps -ef | grep command 或者 ps aux | grep command #查看进程
kill -9 进程id #杀掉对应的进程  
  
   
#### 更高级的用法如下：  
    
    ps aux | grep command | grep -v grep | awk '{print $1}' | xargs kill -9 
#这个表示直接通过command获取进程id并直接kill掉

```bash
ssh root@47.119.134.151
```