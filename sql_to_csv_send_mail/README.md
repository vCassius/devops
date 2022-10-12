###  一、介绍
1)  满足备份 MySQL 表到csv格式 发送到邮箱中
2)  自定义SQL语句满足不同需求
3)  无需依赖命令实现功能
4)  可关闭邮件发送

###  二、使用说明
#### 2.1、下载工具
* 下载 sql_to_mail 文件与 config 放到同一目录中
* 下载地址 https://github.com/G-Akiraka/DevOps/tree/main/sql_to_csv_send_main

#### 2.2、配置文件
* 更具自己使用场景决定

#### 2.3、启动程序
```
./sql_to_mail

2022/10/12 15:57:59 开始创建 CSV 文件
2022/10/12 15:57:59 开始处理： SELECT * from sys_config
2022/10/12 15:57:59 开始处理： SELECT id,name from sys_api;
2022/10/12 15:57:59 处理完毕： sys_config.csv
2022/10/12 15:57:59 处理完毕： sys_api.csv
2022/10/12 15:57:59 SELECT id,name from sys_api;,SELECT * from sys_config 完成!!!
2022/10/12 15:57:59 文件删除成功: sys_api.csv 
2022/10/12 15:57:59 文件删除成功: sys_config.csv 
2022/10/12 15:58:02 邮件发送成功!
2022/10/12 15:58:02 文件删除成功: 库存信息表.zip
```

### 三、其他说明
1)  只支持 MySQL
2)  邮箱没有限制，根据自己需求决定