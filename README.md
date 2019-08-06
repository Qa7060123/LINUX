# LINUX
Linux相关



# 脚本更换软件源
使用
系统要求：CentOS 5+、Ubuntu 14.04+、Debian 7+

使用命令：

## 下载脚本
wget git.io/superupdate.sh
## 运行脚本
bash superupdate.sh

如果第一步你出现错误或执行后无任何输出，请检查是否安装wget和ca-certificates，使用命令：

## Debian、Ubuntu

apt-get install -y wget && apt-get install -y ca-certificates

## CentOS
yum install -y wget && yum install -y ca-certificates

对于Debian默认换源为Fastly CDN的mirror这个源有Fastly的加持对境外主机都有不错的速度。对于Ubuntu和 CentOS系统都默认换为阿里云的mirror，这个源有阿里云全球CDN的加持，全球都有不错的速度。

对于Debian系统还设置了四套其他的源，阿里云，CloudFront CDN，网易163，中科大的源，请根据需要使用参数一键设置如：

bash superupdate.sh cn
bash superupdate.sh 163
bash superupdate.sh aliyun
bash superupdate.sh aws

如果配置的文件不满意，一键还原

bash superupdate.sh restore
