# 🚀 快速开始指南（5分钟上手）

## 选择你的安装方式

### ✅ 最快方式（推荐 ⭐）：Local by Flywheel

**第1步：下载安装** (2分钟)
```
1. 访问：https://localwp.com/
2. 点击"Download Local"
3. 下载Mac版本
4. 拖入Applications文件夹
5. 双击启动
```

**第2步：创建网站** (2分钟)
```
1. 点击"+"按钮
2. 输入名称：lifeCompany
3. 选择"WordPress"
4. PHP 8.2+, MySQL 8.0+
5. 设置管理员账号
```

**第3步：启动开发** (1分钟)
```
1. 点击"Start Site"
2. 点击"WP ADMIN"
3. 登录WordPress后台
✅ 完成！现在就在 http://lifecompany.local/ 可用
```

---

### 🔧 灵活方式：XAMPP命令行

**第1步：安装并启动XAMPP**
```bash
# 使用Homebrew
brew install xampp

# 启动XAMPP（需要管理员权限）
open /Applications/XAMPP/manager-osx.app
# 点击Start: Apache 和 MySQL
```

**第2步：安装WordPress**
```bash
# 进入文件夹
cd /Applications/XAMPP/xamppfiles/htdocs/

# 下载WordPress
curl -O https://wordpress.org/latest.tar.gz

# 解压并重命名
tar -xzf latest.tar.gz
mv wordpress lifecompany
cd lifecompany
```

**第3步：配置WordPress**
```bash
# 复制配置文件
cp wp-config-sample.php wp-config.php

# 编辑配置（用你的编辑器打开）
# 修改这三项：
# define('DB_NAME', 'lifecompany');
# define('DB_USER', 'root');
# define('DB_PASSWORD', '');
```

**第4步：创建数据库**
```bash
# 连接MySQL
mysql -u root

# 执行命令
CREATE DATABASE lifecompany;
EXIT;
```

**第5步：完成安装**
```bash
# 在浏览器打开
open http://localhost/lifecompany/

# 按照引导完成安装
```

---

## 主题与插件快速设置

### 1️⃣ 安装主题

```bash
后台路径：外观 → 主题 → 添加主题

搜索并安装以下主题之一：
✓ Neve（推荐 ⭐⭐⭐⭐⭐）
✓ OceanWP
✓ Natural Herbs Lite

安装后点击"启用"
```

### 2️⃣ 安装核心插件

```bash
后台路径：插件 → 安装插件

按顺序安装并激活：
1. Elementor（页面编辑）
2. Yoast SEO（搜索优化）
3. Contact Form 7（联系表单）
4. WP Super Cache（性能优化）
5. UpdraftPlus（自动备份）
6. Wordfence Security（安全防护）
```

### 3️⃣ 配置主题颜色

```bash
后台路径：外观 → 定制

核心配置5项：
1. 站点标题 → lifeCompany - 中医文化传播
2. Logo上传
3. 主色调 → #2D5016（深绿）
4. 字体 → 微软雅黑（中文）, Poppins（英文）
5. 发布 → 保存变更
```

---

## 快速创建页面

### 页面创建清单

```bash
后台路径：页面 → 新建页面

按以下顺序创建5个页面：
```

#### 1. 首页 (Home)
```
页面标题：首页
页面别名：home
编辑：使用Elementor
内容：
  • 英雄横幅（标题+副标题+背景图）
  • 3个服务卡片（咨询、课程、针灸）
  • 最新文章展示
  • 课程推介
  • 联系按钮
```

#### 2. 博客 (Blog)
```
页面标题：博客
页面别名：blog
编辑：使用Elementor
内容：
  • 添加博客文章列表组件
  • 分类筛选
  • 标签云
```

#### 3. 课程中心 (Courses)
```
页面标题：课程中心
页面别名：courses
编辑：使用Elementor
内容：
  • 课程1卡片：养生基础 ¥999
  • 课程2卡片：针灸入门 ¥1,999
  • 课程3卡片：中医讲座 免费
```

#### 4. 关于我们 (About)
```
页面标题：关于我们
页面别名：about
编辑：使用Elementor
内容：
  • 品牌故事
  • 核心价值观
  • 团队成员介绍
```

#### 5. 联系方式 (Contact)
```
页面标题：联系方式
页面别名：contact
编辑：使用Elementor
内容：
  • Contact Form 7 表单
  • 联系信息卡片
  • 地址、电话、邮箱
  • 工作时间
```

---

## 菜单设置

```bash
后台路径：外观 → 菜单 → 创建菜单

菜单名称：主菜单
添加菜单项：
  • 首页 → 首页
  • 博客 → 博客列表页
  • 课程中心 → 课程中心
    └─ 养生课程
    └─ 针灸培训
    └─ 中医讲座
  • 关于我们 → 关于我们
  • 联系方式 → 联系方式

设置菜单位置：
选择 "Primary Menu" → 点击保存菜单
```

---

## 常见问题速查

| 问题 | 解决方案 |
|------|---------|
| **无法启动Local** | 重启电脑，检查管理员权限 |
| **MySQL无法连接** | 检查wp-config.php中DB_NAME/USER/PASSWORD |
| **页面显示混乱** | 禁用所有插件，逐个启用找出冲突 |
| **图片无法上传** | 运行 `chmod -R 755 wp-content/uploads` |
| **Elementor编辑器白屏** | 在wp-config.php中增加内存: `define('WP_MEMORY_LIMIT', '256M');` |
| **SEO显示0%** | 在Yoast中填写Focus Keyword |

---

## 首次发布内容步骤

### 发布第一篇文章

```bash
后台路径：文章 → 新建文章

1. 标题：输入文章标题
   例如："秋季养生5个要点"

2. 内容：撰写文章内容
   • 至少300字
   • 使用小标题分段
   • 插入相关图片

3. 特色图片：上传文章配图

4. 分类：选择分类
   例如："养生保健"

5. 标签：添加3-5个标签
   例如："秋季", "养生", "健康"

6. SEO设置（Yoast）
   • 焦点关键词：秋季养生
   • Meta描述：最多160字
   • 阅读率：绿色为佳

7. 发布：点击"发布"按钮
```

---

## 性能优化快速指南

### 缓存配置（WP Super Cache）

```bash
后台路径：设置 → WP Super Cache

1. 启用缓存
   □ 启用缓存
   □ 启用对象缓存
   □ 启用浏览器缓存

2. 预加载
   □ 启用缓存预加载

3. CDN（可选）
   □ 启用CDN
```

### 自动备份（UpdraftPlus）

```bash
后台路径：UpdraftPlus → 设置

1. 备份时间表
   • 数据库：每天00:00
   • 文件：每天02:00

2. 备份存储
   • 保留最近的30天备份

3. 测试备份
   点击"立即备份"进行测试
```

---

## SEO初步优化

### 为每个页面配置SEO

```bash
后台各页面/文章编辑页面下方 → Yoast SEO

必填项：
✓ 焦点关键词
✓ Meta标题（50-60字符）
✓ Meta描述（150-160字符）
✓ 阅读友好性检查

目标：所有项目为绿色 ✓
```

### 推荐关键词

| 页面 | 焦点关键词 |
|------|----------|
| 首页 | 中医文化, 养生保健 |
| 博客 | 中医养生知识 |
| 课程 | 中医课程培训 |
| 关于 | 中医传播平台 |
| 联系 | 中医咨询服务 |

---

## 检查列表

完成后请检查：

- [ ] WordPress已安装并可访问
- [ ] 选择的主题已激活
- [ ] 5个核心插件已安装激活
- [ ] 主色调已配置
- [ ] 5个主要页面已创建
- [ ] 菜单已设置并显示正确
- [ ] 至少发布了3篇文章
- [ ] 自动备份已配置
- [ ] SEO基础配置完成
- [ ] 在浏览器中测试所有页面链接正常

---

## 下一步建议

### 第1-2周
- [ ] 继续发布10-15篇高质量文章
- [ ] 优化每篇文章的SEO
- [ ] 收集品牌视觉素材

### 第3-4周
- [ ] 启动社交媒体账号
- [ ] 录制第一个视频内容
- [ ] 准备首期免费讲座

### 第5-6周
- [ ] 上线课程报名系统
- [ ] 启动邮件营销
- [ ] 制定发展计划

---

## 快速参考链接

| 内容 | 链接 |
|------|------|
| WordPress官网 | wordpress.org |
| Local by Flywheel | localwp.com |
| Neve主题 | wordpress.org/themes/neve |
| Elementor | elementor.com |
| Yoast SEO | yoast.com/wordpress/plugins/seo |

---

## 需要帮助？

参考完整指南：
- 📖 `WordPress-Setup-Guide.md` - 详细搭建指南
- 🛠️ `CLI-Reference.md` - 命令行参考
- ✅ `Configuration-Checklist.md` - 配置清单
- 📝 `Content-Planning-Guide.md` - 内容规划

---

**祝你搭建顺利！** 🎉

*如有问题，请查阅完整文档或联系技术支持*

---

版本：v1.0 | 更新：2025年10月16日
