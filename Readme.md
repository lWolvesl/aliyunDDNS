# Readme

### 中文&English

## Java实现阿里云域名DDNS/Implementing alicloud domain name DDNS in Java

## 简介

-   ddns即为动态地址解析
-   正常情况下三大运营商动态分配ip，若将域名直接解析会导致需要经常手动前往域名提供商网页进行修改ip
-   使用ddns可以让服务器自动获取ip，自动修改域名解析映射
-   使用注意前域名需备案

### 1、git clone项目

-   github 
    -   https://github.com/lWolvesl/aliyunDDNS.git
-   gitee
    -   https://gitee.com/lWolvesl/aliyunDDNS.git

### 2、修改resources下的accessKey.properties

![截屏2021-11-26 13.03.26](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.03.26.png)

-   此处的阿里云accesskey可以进入阿里云控制台进行创建，建议使用子账户（本文使用子账户创建）
    -   ![截屏2021-11-26 13.06.50](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.06.50.png)
    -   创建子用户建议保存accessKey和secret，密码只会出现一次
    -   注意为子账户分配权限
    -   ![截屏2021-11-26 13.11.20](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.11.20.png)
-   子域名需要先创建，地址可以随意分配
    -   ![截屏2021-11-26 13.13.32](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.13.32.png)



### 3、使用maven打包

![截屏2021-11-26 12.38.52](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.38.52.png)

-   **ddns-1.0.0-jar-with-dependencies.jar** 为含带所有依赖的jar包，请使用此包进行部署

![截屏2021-11-26 12.39.08](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.39.08.png)

### 4、部署

-   将jar包上传至服务器

![截屏2021-11-26 12.44.36](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.44.36.png)

-   使用nohup实现后台运行并输出日志

![截屏2021-11-26 12.46.27](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.46.27.png)

-   eg：

![截屏2021-11-26 12.48.05](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.48.05.png)

-   此时ddns已成功，

-   使用`ps -ef|grep ddns`可以查看此进程，可用`kill -9 杀死进程`



## brief introduction

-   DDNS is dynamic address resolution
-   Under normal circumstances, the three operators dynamically allocate IP. If the domain name is directly resolved, it will often be necessary to manually go to the domain name provider's web page to modify the IP
-   Using DDNS, the server can automatically obtain IP and modify the domain name resolution mapping
-   Note: the domain name needs to be filed before use

## 1.Git clone project

-   github 
    -   https://github.com/lWolvesl/aliyunDDNS.git
-   gitee
    -   https://gitee.com/lWolvesl/aliyunDDNS.git

## 2.Modify accesskey.properties under Resources

![截屏2021-11-26 13.03.26](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.03.26.png)

-   The alicloud accessKey here can be created on the alicloud console. It is recommended to use a sub account (this article uses a sub account to create it)

![截屏2021-11-26 13.06.50](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.06.50.png)

-   It is recommended to save the accessKey and secret when creating a child user. The password will only appear once
-   Note: assign permissions to sub accounts

![截屏2021-11-26 13.11.20](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.11.20.png)

-   The subdomain name needs to be created first, and the address can be assigned at will
    -   ![截屏2021-11-26 13.13.32](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2013.13.32.png)

## 3.Packaging with maven

![截屏2021-11-26 12.38.52](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.38.52.png)

-   **ddns-1.0.0-jar-with-dependencies.jar** is a jar package with all dependencies. Please use this package for deployment

![截屏2021-11-26 12.39.08](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.39.08.png)

## 4.deploy

-   Upload the jar package to the server

![截屏2021-11-26 12.44.36](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.44.36.png)

-   eg:

![截屏2021-11-26 12.48.05](https://typroa-wolves.oss-cn-hangzhou.aliyuncs.com/img-li/%E6%88%AA%E5%B1%8F2021-11-26%2012.48.05.png)

-   At this time, DDNS has succeeded
-   Use `PS - ef|grep DDNS` to view this process, and use `kill - 9 to kill` the process





## 参考文档/Reference documents

-   阿里云帮助文档中心
    -   https://help.aliyun.com/document_detail/172994.html?spm=a2c1d.8251892.help.dexternal.1fc95b76KMmD6Y