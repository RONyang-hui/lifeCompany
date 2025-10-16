# WordPress快速命令行参考

## wp-cli 命令速查表

### 前置条件
```bash
# 安装wp-cli（如果还未安装）
curl -O https://raw.githubusercontent.com/wp-cli/builds/gh-pages/phar/wp-cli.phar
chmod +x wp-cli.phar
sudo mv wp-cli.phar /usr/local/bin/wp

# 验证安装
wp --version
```

### 站点管理命令

| 功能 | 命令 |
|------|------|
| 获取站点信息 | `wp option get siteurl` |
| 设置站点标题 | `wp option update blogname "lifeCompany"` |
| 获取所有选项 | `wp option list` |

### 用户管理命令

```bash
# 创建新管理员用户
wp user create admin-user email@example.com --role=administrator --user-pass=password123

# 列出所有用户
wp user list

# 重置管理员密码
wp user update 1 --prompt=user_pass
```

### 文章/页面管理命令

```bash
# 创建页面
wp post create --post_type=page --post_title="首页" --post_status=publish --post_content="Welcome"

# 发布文章
wp post create --post_type=post --post_title="我的第一篇文章" --post_status=publish

# 列出所有页面
wp post list --post_type=page

# 列出所有文章
wp post list --post_type=post
```

### 插件管理命令

```bash
# 激活插件
wp plugin activate elementor

# 停用插件
wp plugin deactivate elementor

# 列表所有插件
wp plugin list

# 安装并激活插件
wp plugin install contact-form-7 --activate

# 更新所有插件
wp plugin update --all
```

### 主题管理命令

```bash
# 列出所有主题
wp theme list

# 激活主题
wp theme activate neve

# 安装主题
wp theme install neve --activate

# 获取主题选项
wp option get template
```

### 备份和数据库命令

```bash
# 导出数据库
wp db export /path/to/backup.sql

# 导入数据库
wp db import /path/to/backup.sql

# 清理数据库
wp db repair
wp db clean --all

# 检查数据库
wp db check
```

### SEO相关命令

```bash
# 重新生成XML Sitemap
wp yoast index

# 获取Yoast设置
wp option get wpseo_titles
```

---

## XAMPP 故障排查快速命令

```bash
# 启动所有服务
sudo /Applications/XAMPP/xamppfiles/bin/apachectl start
sudo /Applications/XAMPP/xamppfiles/bin/mysql.server start

# 停止所有服务
sudo /Applications/XAMPP/xamppfiles/bin/apachectl stop
sudo /Applications/XAMPP/xamppfiles/bin/mysql.server stop

# 查看Apache状态
ps aux | grep apache

# 查看MySQL状态
ps aux | grep mysql

# 检查Apache错误日志
tail -f /Applications/XAMPP/xamppfiles/var/log/apache2/error_log

# 检查MySQL错误日志
tail -f /Applications/XAMPP/xamppfiles/var/mysql/error.log

# 查看XAMPP进程
lsof -i -P -n | grep LISTEN
```

---

## 本地测试常用链接

| 页面 | URL |
|------|-----|
| WordPress首页 | http://localhost/lifecompany/ |
| WordPress后台 | http://localhost/lifecompany/wp-admin/ |
| phpMyAdmin | http://localhost/phpmyadmin/ |
| XAMPP主页 | http://localhost/ |

---

*快速参考指南 - 更新于2025年10月16日*
