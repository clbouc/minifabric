# 迷你Fabric
如果您想学习Hyperledger Fabric或开发智能合约，或者只是想了解
Hyperledger Fabric，迷你Fabric是让您快速开始的良好工具。迷
你Fabric可以用来在配置很小的电脑像VirtualBox上的一个虚机上为
您搭建Fabric网络，但也可以在多个大型机器上部署多节点Fabric网络。
迷你Fabric虽然很小，但它可以让您体验Hyperledger Fabric的全部
功能，比如channel创建，channel加入，链码安装，批准，实例化等。
它还支持channel更新，私有数据收集，块查询等。您只需要的是[docker](https://www.docker.com/)（18.03或更高版本）环境。
迷你Fabric可在OS X, Linux和Windows上运行。 对于那些急于上手的人，请按照
以下步骤开始操作，或参考[教学视频](https://v.youku.com/v_show/id_XNDYyMDU2OTY3Mg==.html?spm=a2hzp.8244740.0.0&f=52423582)

如果您想在动手之前了解更多信息，请阅读[迷你Fabric用户指南(原文)](https://github.com/litong01/minifabric/blob/master/docs/README.md)。


### 下载工具

#### 如果你所在地难于访问境外的网站
下载下面三个文件
1. https://share.weiyun.com/5l2rQhO
2. https://share.weiyun.com/5sfKniB
3. https://share.weiyun.com/5bDTjJE

把第一个文件命名为minifaball.tgz, 把第二个文件命名为minifab,把第三个文件命名为chaincode.tgz 然后执行下面三个命令
```
cat minifaball.tgz | docker load
chmod +x minifab
mkdir vars && tar -xvf ~/chaincode.tgz -C vars
```

#### 如果你所在地容易访问境外网站

#### 如果你使用Linux或OS X系统
```
mkdir -p ~/mywork && cd ~/mywork && curl -o minifab -sL https://tinyurl.com/twrt8zv && chmod +x minifab
```
#### 如果你使用Windows 10系统
```
md %userprofile%\mywork & cd %userprofile%\mywork & curl -o minifab.cmd -sL https://tinyurl.com/yb3ouwm3
```

### ### 搭建Fabric网络:

#### 如果你使用Linux或OS X系统
```
./minifab up
```

#### 如果你使用Windows 10系统
```
minifab up
```

### 删除Fabric网络:
#### 如果你使用Linux或OS X系统
```
./minifab down
```

#### 如果你使用Windows 10系统
```
minifab down
```
注意: 如果你使用Windows系统，命令行参数中所有双引号必须使用`\"`来代替。比如：
```
  minifab invoke -p '"invoke","a","b","4"'
```
必须变成下面
```
  minifab invoke -p \"invoke\",\"a\",\"b\",\"4\"
```


