#### 创建者：xtbaige  
##### 更新时间：2024-1-20 23:49:04
#### 感谢大家一路支持 [卖货的老张]  

## 目前最简单、最安全、最稳定的专属节点搭建方法  

### 安装X-UI面板  
    bash <(curl -Ls https://raw.githubusercontent.com/FranzKafkaYu/x-ui/956bf85bbac978d56c0e319c5fac2d6db7df9564/install.sh) 0.3.4.4

##放行端口  
       iptables -I INPUT -p tcp --dport 443 -j ACCEPT  

FinalShell下载：  
    https://wa6.lanzoui.com/ihjg2y3h14j  
### 各平台客户端  
Windows（v2rayN）：https://github.com/2dust/v2rayN/releases/tag/6.23  

Android（v2rayNG）：https://github.com/2dust/v2rayNG/releases/tag/1.8.5  

IOS（shadowrocket）：https://apps.apple.com/app/shadowrocket/id932747118  

订阅转换：https://acl4ssr-sub.github.io/  

#### 搭建vision节点申请证书  
#安装证书工具：  

curl https://get.acme.sh | sh; apt install socat -y || yum install socat -y; ~/.acme.sh/acme.sh --set-default-ca --server letsencrypt

#三种方式任选其中一种，申请失败则更换方式  
#申请证书方式1：   
~/.acme.sh/acme.sh  --issue -d 你的域名 --standalone -k ec-256 --force --insecure
#申请证书方式2：   
~/.acme.sh/acme.sh --register-account -m "${RANDOM}@chacuo.net" --server buypass --force --insecure && ~/.acme.sh/acme.sh  --issue -d 你的域名 --standalone -k ec-256 --force --insecure --server buypass
#申请证书方式3：   
~/.acme.sh/acme.sh --register-account -m "${RANDOM}@chacuo.net" --server zerossl --force --insecure && ~/.acme.sh/acme.sh  --issue -d 你的域名 --standalone -k ec-256 --force --insecure --server zerossl

#安装证书：  
~/.acme.sh/acme.sh --install-cert -d 你的域名 --ecc --key-file /etc/x-ui/server.key --fullchain-file /etc/x-ui/server.crt  
