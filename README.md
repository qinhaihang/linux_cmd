# linux_cmd

#### 关闭终端之后继续运行
```
nohup ./test.sh &
```
> 后台运行则不用 nohup

#### 创建（删除）文件(夹)

   1. 创建文件： touch a.txt
   2. 创建文件夹： mkdir NewFolder
   3. 删除文件： rm a.txt
   4. 删除文件夹： rmdir NewFolder
   5. 删除带有文件的文件夹： rm -r NewFolder
   
#### 安装Intellij Idea 
1. 切换到下载目录
2. 解压到指定目录 ```sudo tar -zxvf ideaIU-2016.3.3-no-jdk.tar.gz -C /opt```
3. 切换到 /opt目录 
   ```
   cd /opt/idea-IU-163.11103.6/bin
   ```
4. 运行 
   ```
   ./idea.sh
   ```
   
 #### 安装Android Studio
 > 一篇参考文章</br>
 https://qianngchn.github.io/wiki/8.html
 ```
 sudo cp android-studio-ide-171.4408382-linux.zip /opt
 sudo unzip -x android-studio-ide-171.4408382-linux.zip (解压，可以用 tar命令)
 cd android studio/bin
 sudo gedit idea.porperties （需要通过 sudo chmod 777 idea.porperties ）
 cd /opt/android studio
 sudo chmod 777 bin
 运行 ./studio.sh
 ```
 1. 配置环境变量
 ```
//打开
sudo gedit ~/.bashrc 
或者 
sudo /etc/profile
 ```
 ```
#android stdio
export ANDROID_HOME=/opt/android-studio/bin
export PATH=$PATH:$ANDROID_HOME
 ```
#### 修改文件以及文件夹名称
```
//修改文件名
sudo mv former_name new_name
//修改文件夹名
sudo mv former_name/ new_name/
```

#### 打开 pdf以及doc文档
```
//打开PDF
evince [filename] &

//打开doc
libreoffice filename &
```
https://blog.csdn.net/www_helloworld_com/article/details/84786581

#### java jdk 配置
查看安装路径 </br>
sudo update-alternatives --config java </br>
环境变量配置 </br>
1、 如果使用oracle java
export JAVA_HOME="/usr/lib/jvm/java-8-oracle/jre/bin"

2、 如果使用openjdk
export JAVA_HOME="/usr/lib/jvm/java-8-openjdk-amd64/jre/bin"

https://blog.csdn.net/demonliuhui/article/details/77488296

#### 解压zip文件夹
```
语法：unzip 〔选项〕 压缩文件名.zip

  各选项的含义分别为：

  -x 文件列表 解压缩文件，但不包括指定的file文件。

  -v 查看压缩文件目录，但不解压。

  -t 测试文件有无损坏，但不解压。

  -d 目录 把压缩文件解到指定目录下。

  -z 只显示压缩文件的注解。

  -n 不覆盖已经存在的文件。

  -o 覆盖已存在的文件且不要求用户确认。

  -j 不重建文档的目录结构，把所有文件解压到同一目录下。

  例1：将压缩文件text.zip在当前目录下解压缩。

  $ unzip text.zip

  例2：将压缩文件text.zip在指定目录/tmp下解压缩，如果已有相同的文件存在，要求unzip命令不覆盖原先的文件。

  $ unzip -n text.zip -d /tmp

  例3：查看压缩文件目录，但不解压。

  $ unzip -v text.zip
```

