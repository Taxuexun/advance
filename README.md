Yii 权限管理 GII
===============================

- 安装方法 （必须安装composer 建议linux系统）
    * composer安装方法

            http://docs.phpcomposer.com/

    * 克隆代码

            dev环境：git@github.com:Taxuexun/advance.git

    * 初始化环境

            在项目根目录下 执行 php init (需将php.exe加入环境变量 或者 绝对路径)
            执行后会出现选项0为开发环境 1为生产环境

    * 更新composer包

            项目目录执行 composer update 如更新失败 先composer install

    * 更新代码

            再从git仓库 更新一下代码 (git pull)
            
    * 修改数据库配置
   	   对应修改database配置 
          
    * 入口文件
        
            在对应项目的目录 web 下的入口文件index.php中加入以下代码
                    
    * 配置服务器（nginx）

            server中加入以下代码来隐藏路由中index.php
            location / {
                 try_files $uri $uri/ /index.php?$args;
            }

    * 配置服务器（apache）

            Directory 中加入以下代码来隐藏路由中index.php
            RewriteEngine on
            RewriteCond %{REQUEST_FILENAME} !-f
            RewriteCond %{REQUEST_FILENAME} !-d
            RewriteRule . index.php





