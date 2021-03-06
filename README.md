# centos7-deep
Setup Deep Learning Environment on CentOS 7

# 系统配置和准备
- 支持cuda的显卡
- 干净安装的CentOS 7  
- 用一个带无需密码的sudo权限的用户登陆[(怎么搞?)](http://serverfault.com/questions/160581/how-to-setup-passwordless-sudo-on-linux)
- 去[这里](https://developer.nvidia.com/cudnn)注册并下载cuDNN
- 去[这里](http://www.nvidia.com/Download/index.aspx)下载NVidia显卡驱动

```
git clone https://github.com/aaalgo/centos7-deep.git
```

把cudnn-7.0-linux-x64-v3.0-prod.tgz放入centos7-deep目录底下

# 安装基本系统

运行下面的命令将安装cuda, theano, lasagne, tensorflow以及各种必须的包
```
cd centos7-deep
./install1.sh
```

重启机器, 安装显卡驱动

```
./NVIDIA-Linux-x86_64-361.28.run # 下载的nvidia显卡驱动


cd centos7-deep
./install2.sh
```

# 安装mxnet

```
./install-mxnet.sh
```

# 安装Caffe
```
./install-caffe.sh
```

# 安装Nirvana neon
```
./install-neon.sh
```

注意neon只支持virtualenv安装, 需要用. $HOME/.neon/bin/activate激活virtualenv

