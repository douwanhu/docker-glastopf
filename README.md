# dockerized glastopf v3

## 一、项目介绍<br>
[glastopf](https://github.com/glastopf/glastopf) 是基于python的web型蜜罐。<br>
此项目是将glastopf制作成docker镜像，包含定制该蜜罐的配置文件以及build docker镜像的Dockerfile。<br>
此项目作为多蜜罐项目 **[Multi-Honeypots]** 的一个蜜罐部件。<br>

## 二、蜜罐介绍<br>

glastopf蜜罐可以针对已知和未知的漏洞给出响应，通过维护Dork列表吸引攻击者。<br>
通过PHP沙盒支持远程文件包含，虚拟文件系统支持本地文件包含，通过POST请求<br>
实现HTML注入。支持对SQL注入的分类和解析。

## 三、威胁数据<br>

所有的威胁数据存储至/data/glastopf/下<br>
log存储至/data/glastopf/galstpof.log，主要记录了请求的细节<br>
更详实的记录以DB的形式保存至 /data/glastopf/db/glastpof.db<br>

为避免磁盘空间占用过大，多蜜罐系统默认24小时重启一次，且重启后清除<br>
/data/下的数据，并在清除之前将所有数据导入到已部署的MySQL数据库中<br>

附在公网上90天cowrie捕获到的威胁数据统计报告dashboard<br>
![Glastopf Dashboard](https://raw.githubusercontent.com/douwanhu/docker-glastopf/master/doc/dashboard.png)

