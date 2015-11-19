# 说明
 1. 原始代码源于优酷开放平台的上传 PHP SDK，原版本最后更新日期 **2013-12-09**，[官方链接](http://open.youku.com/down)
 2. 原官方代码存在问题，这里仅对自己在使用过程中遇到的问题做出错误修正维护。
 
# 补充，Nginx+PHP上传文件参数配置
优酷允许上传最大限制是1G，根据该要求，可以如下配置
## Nginx设置 nginx.conf文件
  http项内添加
```conf
  client_max_body_size 1024M
```
## PHP中设置php.ini
```ini
  post_max_size 1024m
  upload_max_filesize 1024m
  max_execution_time 600
  max_input_time 600
  memory_limit 128M
```
