## Typora结合PicGo-Core将本地图片上传到github



### PicGo-Core下载

1. 打开`偏好设置`，如下图所示

   ![image-20200829213704513](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829213704513.png)

   

2. 找到`图像`设置栏，如下图`1`处

   1. 然后在下图的`2`处选择`PicGo-Core(Command line)`
   2. 然后点击下图`3`处进行`PicGo-Core`的下载，这通常需要穿墙，否则极大概率下载失败
   3. 待`PicGo-Core`下载完成之后，点击下图`4`处进行上传的配置

   ![image-20200829214421816](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829214421816.png)



### 图床配置

1. 在上述步骤打开了配置文件之后，复制一下内容到文件中，并根据自己的实际情况进行配置

   ```json
   {
     "picBed": {
       "current": "github",
   
       "uploader": "github",
   
       "github":{
           "repo": "用户名/仓库名", // 仓库名，格式是 username/reponame
           "token": "", // github token
           "path": "img/", // 自定义存储路径，比如 img/
           "customUrl": "https://cdn.jsdelivr.net/gh/用户名/仓库名", // 自定义域名，注意要加 http://或者 https://
           "branch": "master" // 分支名，默认是 master
       }
     },
   
     "picgoPlugins": {}
   }
   
   ```

   

2. 上面的配置中需要一个`token`,这个`token`的获取步骤如下

   1. 访问[https://github.com/settings/tokens](https://github.com/settings/tokens)

   2. 点击`Generate new token`

      ![image](https://cdn.jsdelivr.net/gh/Square-John/Image/img/generate_new_token.png)

      

   3. 然后只需要将`repo`勾上，其他的保持默认

   4. 找到最底部的`Generate token`绿色按钮生成`token`

      ![image](https://cdn.jsdelivr.net/gh/Square-John/Image/img/20180508210435.png)

      

   5. 将获得的`token`进行及时复制跟保存，因为这个`token`只会显示一次

      ![image](https://cdn.jsdelivr.net/gh/Square-John/Image/img/copy_token.png)

      

3. 保存关闭文件，配置到此结束



### 测试

1. 点击如下按钮，等待测试完成

   ![image-20200829220316405](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829220316405.png)

   

2. 如果一段时间后结果如下，表明图床配置成功，否则配置失败

3. ![image-20200829220246677](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829222003008.png)



### 图片上传

1. 床配置成功之后，以后就可以选中某一张图片右键选择`上传图片`将指定的图片上传，并会在上传成功之后将本地图片链接自动转换为服务器上的远程图片链接，如下图

   ![image-20200829221614471](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829220246677.png)

   

2. 还可以批量上传当前文件中的所有图片，只需要按如下图步骤操作即可

   ![image-20200829222003008](https://cdn.jsdelivr.net/gh/Square-John/Image/img/image-20200829221614471.png)



### END