# AI Play on Ubuntu Platform

AI实验环境搭建和深度学习算法安装实验     
      
**安装环境**  
*其他环境类似* 
```
硬件环境: CPU i7 / NVIDIA TITAN V / SSD
系统环境：Ubuntu 16.04 64bit
安装软件：CUDA9.0 / caffe / YOLO V3 / Protobuf / Matlab / VIM
````
---
### 目录
1. [**AI基础环境搭建和设置**](src/ai_base_env.md#ai基础环境搭建和设置)
   1. [安装Ubuntu和Windows双系统](src/ai_base_env.md#安装ubuntu和windows双系统)   
   2. [安装**NVIDIA驱动**](src/ai_base_env.md#安装nvidia驱动)   
       - [安装NVIDIA驱动所需的依赖包](src/ai_base_env.md#安装nvidia驱动所需的依赖包)   
       - [禁用Ubuntu自带的显卡驱动](src/ai_base_env.md#禁用ubuntu自带的显卡驱动)   
       - [安装NVIDIA官方显卡驱动](src/ai_base_env.md#安装nvidia官方显卡驱动)   
       - [配置NVIDIA环境变量](src/ai_base_env.md#配置环境变量)   
       - [查看NVIDIA显卡驱动版本](src/ai_base_env.md#查看NVIDIA驱动版本)  
   3. [安装**CUDA**](src/ai_base_env.md#安装cuda)   
       - [安装CUDA步骤](src/ai_base_env.md#安装cuda步骤)    
       - [修改配置文件](src/ai_base_env.md#修改配置文件)    
       - [查看CUDA版本](src/ai_base_env.md#查看cuda版本)
       - [卸载CUDA的方法](src/ai_base_env.md#卸载cuda的方法)    
   4. [安装**cuDNN**](src/ai_base_env.md#安装cudnn)    
   5. [**CUDA多版本**问题](src/ai_base_env.md#cuda多版本问题)
   6. [**Anaconda**](src/ai_base_env.md#anaconda)    
       - [安装Anaconda](src/ai_base_env.md#安装anaconda)    
       - [屏蔽Anaconda](src/ai_base_env.md#屏蔽anaconda)    
       - [重建Anaconda软连接](src/ai_base_env.md#重建anaconda软连接)
       - [Anaconda虚拟环境](src/ai_base_env.md#anaconda虚拟环境)
   7. [安装**OpenCV**](src/ai_base_env.md#安装opencv)   
       - [下载OpenCV](src/ai_base_env.md#下载opencv)
       - [编译OpenCV](src/ai_base_env.md#编译opencv)
       - [安装OpenCV](src/ai_base_env.md#安装opencv)
       - [卸载OpenCV](src/ai_base_env.md#卸载opencv)
   8. [**TensorRT**](src/ai_base_env.md#tensorrt) 
       - [安装TensorRT](src/ai_base_env.md#安装tensorrt)    
         - [TensorRT环境变量设置](src/ai_base_env.md#tensorrt1)
         - [安装Python的TensorRT包](src/ai_base_env.md#tensorrt2)
         - [安装uff](src/ai_base_env.md#tensorrt3)
         - [验证TensorRT是否安装成功](src/ai_base_env.md#tensorrt4)
         - [TensorRT安装过程中遇到的问题以及解决方法](src/ai_base_env.md#tensorrt5)
       - [TensorRT生成Engine](src/ai_base_env.md#tensorrt生成engine)
         - [TensorRT Caffe Engine](./src/tensorrt/tensorrt-4.0.1.6/caffe_to_tensorrt.ipynb)
         - [TensorRT Tensorflow Engine](./src/tensorrt/tensorrt-4.0.1.6/tf_to_tensorrt.ipynb)
         - [Manually Construct Tensorrt Engine](./src/tensorrt/tensorrt-4.0.1.6/manually_construct_tensorrt_engine.ipynb)
   9.  [安装**Caffe**](src/ai_base_env.md#安装caffe)   
       - [Python2下安装Caffe](src/ai_base_env.md#python2下安装cafe) 
       - [Python3下安装Caffe](src/ai_base_env.md#python3下安装cafe )
   10. [安装Protobuf](src/ai_base_env.md#安装protobuf)
   11. [Linux MATLAB安装](src/ai_base_env.md#linux-matlab安装)

2.  [**AI Algorithms**](./src/ai_algorithms.md)
     - [YOLO V3](src/ai_algorithms.md#yolo-v3)
     - [Faster R-CNN](./src/ai_algorithms.md#faster-r-cnn)
     - [Anaconda FAQ](./src/ai_algorithms.md#anaconda-faq)
       - [Anaconda环境下TensorFlow和Pytorch共存问题](./src/ai_algorithms.md#anaconda环境下tensorflow和pytorch共存问题)
       - [Anaconda环境下Python下导入正常Jupyter Notebook中导入莫名出错](./src/ai_algorithms.md#anaconda环境下python下导入正常jupyter-notebook中导入莫名出错)
     - [深度学习服务器FAQ](./src/ai_server_FAQ.md#深度学习服务器faq)
       - [docker常用命令](./src/ai_server_FAQ.md#docker常用命令) 
       - [多显卡训练问题](./src/ai_server_FAQ.md#多显卡训练问题) 
       - [远程访问服务器**Jupyter Notebook**](./src/ai_server_FAQ.md#远程访问服务器jupyter-notebook)
         - [方法1 ssh远程使用jupyter notebook](./src/ai_server_FAQ.md#方法1-ssh远程使用jupyter-notebook)
         - [方法2 利用jupyter notebook自带的远程访问功能](./src/ai_server_FAQ.md#方法2-利用jupyter-notebook自带的远程访问功能)

3.  [**AI Framework**](src/ai_framework.md#ai-framework)
    - [TensorFlow](src/ai/tensorflow.md#tensorflow)
    - [Pytorch](src/ai/pytorch.md#pytorch)
      - [将数据转换为Pytorch格式](src/ai/pytorch.md#将数据转换为pytorch格式)

4.  [**Ubuntu FAQ**](./src/linux_env_set.md#ubuntu-faq)
     - [**Docker**安装与使用](./src/linux_env_set.md#docker安装与使用)
       - [Docker安装](./src/linux_env_set.md#docker安装)
       - [Docker使用](./src/linux_env_set.md#docker使用)
     - [**Linuxbrew**安装](./src/linux_env_set.md#linuxbrew安装)
       - [安装linuxbrew](./src/linux_env_set.md#安装linuxbrew)
       - [linuxbrew必装包](./src/linux_env_set.md#linuxbrew必装包)
       - [brew常用命令](./src/linux_env_set.md#brew常用命令)
       - [linuxbrew注意事项](./src/linux_env_set.md#linuxbrew注意事项)
     - [监视GPU和CPU资源利用情况](./src/linux_env_set.md#监视gpu和cpu资源利用情况)
     - [Ubuntu每次开机后提示检测到系统程序出现问题的解决方法](./src/linux_env_set.md#ubuntu每次开机后提示检测到系统程序出现问题的解决方法)
     - [Ubuntu循环登陆问题](./src/linux_env_set.md#ubuntu循环登陆问题)
     - [安装Python依赖库](./src/linux_env_set.md#安装python依赖库)
       - [Python基础库安装](./src/linux_env_set.md#python基础库安装)
       - [Python项目requirements文件的生成和使用](./src/linux_env_set.md#python项目requirements文件的生成和使用) 
     - [安装Chrome浏览器](./src/linux_env_set.md#安装chrome浏览器)
     - [pip/pip3安装报错问题](./src/linux_env_set.md#pip和pip3安装报错)
     - [关于Ubuntu 16.04LTS下安装Spyder3的问题](./src/linux_env_set.md#ubuntu-16下安装spyder3)
     - [安装搜狗输入法](./src/linux_env_set.md#安装搜狗输入法)
     - [WPS无法输入中文](./src/linux_env_set.md#wps无法输入中文)
     - [安装赛睿霜冻之蓝V2驱动](./src/linux_env_set.md#安装赛睿霜冻之蓝v2驱动)
     - [**zsh** **oh-my-zsh**默认shell的最佳替代品](./src/linux_env_set.md#zsh-oh-my-zsh默认shell的最佳替代品)
       - [查看系统shell环境](./src/linux_env_set.md#查看系统shell环境)
       - [安装zsh](./src/linux_env_set.md#安装zsh)
       - [安装vimrc](./src/linux_env_set.md#安装vimrc)
       - [安装oh-my-zsh](./src/linux_env_set.md#安装oh-my-zsh)
       - [安装zsh-syntax-highlighting](./src/linux_env_set.md#安装zsh-syntax-highlighting)
       - [安装**colorls**](./src/linux_env_set.md#安装colorls)
     - [**vim**配置](./src/linux_env_set.md#vim配置)
       - [YouCompleteMe实现vim自动补全](./src/linux_env_set.md#youcompleteme实现vim自动补全)
       - [vim最终配置](./src/linux_env_set.md#vim最终配置)
     - [**Tmux**配置与使用](./src/linux_env_set.md#tmux配置与使用)
       - [Tmux配置](./src/linux_env_set.md#tmux配置)
       - [Tmux使用手册](./src/linux_env_set.md#tmux使用手册)
     - [**Sublime Text 3**配置问题](./src/linux_env_set.md#sublime-text-3配置问题)
     - [**VSCode**配置问题](./src/linux_env_set.md#vscode配置问题)    
       - [VScode推荐插件](./src/linux_env_set.md#vscode推荐插件)
       - [VScode环境配置](./src/linux_env_set.md#vscode环境配置)
     - [Ubuntu查看和关闭进程](./src/linux_env_set.md#ubuntu查看和关闭进程)
     - [Ubuntu后台执行命令](./src/linux_env_set.md#ubuntu后台执行命令)   
     - [查看系统状态](./src/linux_env_set.md#查看系统状态)
     - [**Shadowsocks**安装](./src/ss.md#shadowsocks安装)
       - [Shadowsocks说明](./src/ss.md#shadowsocks说明)
       - [安装Shadowsocks-qt5](./src/ss.md#安装shadowsocks-qt5)
       - [安装electron-ssr](./src/ss.md#安装electron-ssr)
       - [配置Chrome浏览器](./src/ss.md#配置chrome浏览器)

5.  [**参考资料**](#参考资料)


---
##  参考资料  
> 1. [win10下安装Ubuntu16.04双系统](https://blog.csdn.net/s717597589/article/details/79117112/)
> 2. [Ubuntu 16.04+CUDA 9.1+cuDNN v7+OpenCV 3.4.0+Caffe+PyCharm 完全安装指南](https://blog.csdn.net/balixiaxuetian/article/details/79154013)
> 3. [cuDNN官方安装指导](https://docs.nvidia.com/deeplearning/sdk/cudnn-install/index.html#installlinux)
> 4. [Install caffe with anaconda(3.6) on ubuntu16.04](http://www.yaoingwen.com/ubuntu16-04-anaconda-3-6-caffe/)
> 5. [caffe编译遇到的问题](https://blog.csdn.net/m0_37407756/article/details/70789271)
> 6. [linux安装MATLAB R2018a步骤](https://blog.csdn.net/m0_37775034/article/details/80876362) 
> 7. [关于Ubuntu16.04LTS下Python版本和安装Spyder3的问题？](https://www.zhihu.com/question/51248022/answer/142596984)
> 8. [zsh + oh-my-zsh 默认shell的最佳替代品](https://blog.phpgao.com/oh-my-zsh.html)
> 9. [Terminal Experience](https://medium.com/@caulfieldOwen/youre-missing-out-on-a-better-mac-terminal-experience-d73647abf6d7)
> 10. [远程访问服务器Jupyter Notebook的方法](https://www.jianshu.com/p/8fc3cd032d3c)    
> 11. [Jupyer Notebook官方指南](https://jupyter-notebook.readthedocs.io/en/latest/public_server.html#notebook-server-security)
> 12. [设置 jupyter notebook 可远程访问](https://blog.csdn.net/simple_the_best/article/details/77005400)
> 13. [Docker — 从入门到实践](https://github.com/yeasy/docker_practice)
> 14. [Docker 官方 Ubuntu 安装文档](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
> 15. [.tmux配置](https://github.com/gpakosz/.tmux)
> 16. [Tmux 快捷键 & 速查表](https://gist.github.com/ryerh/14b7c24dfd623ef8edc7)
> 17. [TensorRT官方安装指南](https://docs.nvidia.com/deeplearning/sdk/tensorrt-install-guide/index.html)
