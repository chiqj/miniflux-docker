# miniflux-docker

使用 Docker 部署 Miniflux，包含 Nginx 配置。

# 准备

```
git clone https://github.com/chiqj/miniflux-docker.git
```

# 创建环境变量配置文件

进入项目根目录，创建 `.env` 文件，内容如下：

```
# 访问应用的地址，用于设置 cookie
BASE_URL=https://example.com/

# miniflux 管理员帐号和密码
ADMIN_USERNAME=your_name
ADMIN_PASSWORD=your_password

# 数据库帐号和密码
POSTGRES_USER=your_name
POSTGRES_PASSWORD=your_password
```

# docker-compose 启动

进入项目根目录

```
docker-compose up -d
```

# 设置 Nginx 代理

```
sudo cp nginx.conf /etc/nginx/sites-enabled/miniflux.conf
sudo nginx -s reload
```
