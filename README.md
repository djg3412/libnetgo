# libNetGo (Linux网络分析工具)

> libNetGo特点

- 支持Console和Web方式输出
- 实时显示TCP 连接源/目标/用户/进程
- 实时显示进/出网络包统计
- Golang+websocket开发
- API接口Json数据输出和网络包统计开关控制

> libNetGo命令行输出

![libnetgo](https://github.com/gotoolkits/libnetgo/blob/master/pics/pic1.png)


> libNetGo WebUI输出

![libnetgo](https://github.com/gotoolkits/libnetgo/blob/master/pics/pic2.png)


> 安装

- 依赖安装：  libpcap（数据包捕获函数库）

```
 yum install libpcap-devel
 yum install tcpdump
```

- libNetGo 源码安装

```
  go get github.com/gotoolkits/libnetgo 
  cd $GOPATH/src/github.com/gotoolkits/libnetgo
  go build -o libnetgo libnet.go
```

>  执行参数说明

```
libnetgo [-hs] [-ip ipAddr] [-r interval] [-t all/remote/local]

  -h	帮助
  -c	开启Console输出
  -ip   指定网络包统计接口IP地址
  -r    统计与显示间隔（默认3秒）
  -s	开启API服务（默认开启true，false/true）
  -t    输出的TCP连接类型 （all/remote/local 默认"all")
```

>  使用演示

![libnetgo](https://github.com/gotoolkits/libnetgo/blob/master/pics/libnetgo_1.gif)

