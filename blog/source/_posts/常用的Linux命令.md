---
title: 常用的Linux命令
date: 2020-09-16 20:34:47
tags:
---
**常用的Linux命令**：

1. **whoami** 查看当前用户名
2. **which nginx** 查看nginx等用户安装程序、命令的位置及是否存在
3. **whereis cat** 查看cat等系统程序、命令的位置及是否存在
4. **pwd** 查看当前文件夹完整路径
5. **mv a b** 将文件 a 重命名为 b
6. **cp a b** 将文件 a 复制一份命名为 b
7. **du -h --max-depth=1** 查看文件内存（mac：du -shc *）
8. **netstat -ntpl** 查看本机所有端口进程
9. **telnet ip port** 测试远程主机端口连通性
10. **tar -zcvf dist.tar.gz dist** 当前文件夹下压缩dist
11. **ps -aux | grep node** 查看node进程
12. **kill -9 20713** 杀掉20713进程
13. **tail -f filename** 始终显示文件名为filename里最尾部的内容，并且不断刷新
14. **tail -n 10 filename** 显示文件名为filename里最新的最后10行内容
15. **ssh -p 2222 user@host** 使用user用户登录host主机的2222端口
16. **su admin** 当前用户切成admin（sudo类似）
17. **scp -P 9527 user@ip:/path/dist ./** 使用user用户身份，将地址为ip的主机下path目录里的dist发送到当前目录下
18. **sz dist** 下载dist文件（rz上传）
19. **open filename** 使用系统默认的程序打开filename文件
20. **find -name test.txt**（find <指定目录> <指定条件> <指定动作>）
21. **locate test.txt** 在系统后台数据库中按文件名搜索test.txt的完整路径（有坑，依赖于/var/db/locate.database 是否存在）
22. **curl 127.0.0.1:3000** 在本服务器上访问起的3000端口服务（wget 跟 curl 类似）
23. **top** 命令式系统性能分析工具，作用跟Windows任务管理器和 Mac 活动监视器差不多
24. **host** DNS查询工具（**nslookup** / **dig**查的信息比 host 更加完整）
25. **history** 查看最近使用的命令行历史记录
26. **vim/vi** [filename]、wq 和 q!   在命令行编辑一个文件，并保存退出/不保存退出
27. **cat** filename  在命令行打印出一个文件内容
28. **ls | grep \*.js**   筛选出当前文件夹所有的 js后缀名的文件（| 是管道操作符，grep 是过滤操作符）
29. **lsof -i tcp:8080** 快速找到 8080 端口的进程号（解决端口占用问题）
30. **nginx -t**  nginx-conf 路径
31. **dig** DNS查询过程。  @指定dns服务器
32. **dig -x 192.30.252.153**  查询PRT记录 用于从IP地址反查域名    简化：host 
33. **nslookup** 用于互动式的查询域名记录
34. **curl ipinfo.io/json** 外网ip  内网 ifconfig
35. **tail -f access.log** 查看实时日志
36. **ln -s a b** 中的 a 就是源文件，b是链接文件名,其作用是当进入b目录，实际上是链接进入了a目录  软链