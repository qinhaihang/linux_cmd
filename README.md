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
#android stdio
export ANDROID_HOME=/opt/android-studio/bin
export PATH=$PATH:$ANDROID_HOME
 ```
