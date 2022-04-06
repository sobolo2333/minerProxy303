# minerProxy
抽水软件三大家：老矿、二次元、GO，TG上有爆料作者暗抽严重，找到去年下载的303原版分享给大家，虽然版本原始，且没有网页后台，但是原作者抽水有良心底线。
## 知识是财富
根据下面指令无法操作的可以联系【电报https://t.me/Pure_minerProxy303 QQ群496875829】帮你搭建，可以添加隧道加密数据传输、混淆加密数据传输。

## Liunx下

```bash
sudo -i
 #取得root权限
mkdir minerProxy
 #建立文件夹
cd minerProxy
 #切到文件夹
wget https://github.com/sobolo2333/minerProxy303/archive/refs/tags/303.tar.gz
 #下载
tar -xzvf 303.tar.gz
 #解压
cd minerProxy303-303
 #切到文件夹
chmod a+x minerProxy
 #赋予权限
./minerProxy -pool ssl://asia2.ethermine.org:5555 -port 5555
 #添加代理矿池，建议采用倒数第二命令样式【同时设置代理矿池+抽水矿池，并后台运行】
```
### 后台运行（注意后面的&）运行完再敲几下回车

```bash
nohup ./minerProxy -pool ssl://asia2.ethermine.org:5555 -port 5555 &
```

### 后台运行时关闭

```bash
killall minerProxy
```

### 后台运行时查看

```bash
tail -f nohup.out
```

### 要运行多个代理矿池,设置不同的本地端口即可,例如

```bash
cd /root/minerProxy/minerProxy303-303
#切到软件目录(添加代理、添加抽水参数都需要切到软件目录）
```

```bash
nohup ./minerProxy -pool ssl://ethssl-asia.f2pool.com:6698 -port 6698 &
```
## 提示bash: git: command not found的先安装git
### ubuntu下

```bash
apt update
apt install git
```

### centos下

```bash
yum update
yum install git
```

## Windows-CMD下

```bash
minerProxy.exe -pool ssl://asia2.ethermine.org:5555 -port 5555
```

# 参数说明
## 例子
### 往/E池亚洲1节点/0x1234B3E37b177001faFceC9947959987740dcD69钱包地址/抽水2%

```bash
./minerProxy -devPool ssl://asia1.ethermine.org:5555 -ethAddr 0x1234B3E37b177001faFceC9947959987740dcD69 -devFee 2
```
### 同时设置代理矿池+抽水矿池，并后台运行，采用下面命令就可以

```bash
nohup ./minerProxy -pool ssl://asia2.ethermine.org:5555 -port 5555 -devPool ssl://asia1.ethermine.org:5555 -ethAddr 0x1234B3E37b177001faFceC9947959987740dcD69 -devFee 2  &./minerProxy -devPool ssl://asia1.ethermine.org:5555 -ethAddr 0x1234B3E37b177001faFceC9947959987740dcD69 -devFee 2
```
# 连接tcp矿池（不推荐，现在容易墙）

```bash
./minerProxy -pool tcp://ethash.poolbinance.com:3333
```
