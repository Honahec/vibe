# Vibe

一个由 Next.js 驱动的现代社交媒体应用，具有实时交互功能和精美的响应式界面。

## 主要功能

- **用户认证**：基于 Clerk 的安全用户认证系统
- **帖子功能**：支持创建、阅读、点赞和评论帖子，包含图片上传功能
- **个人资料管理**：可自定义的用户资料，包括个人简介、位置和网站链接
- **社交互动**：关注/取消关注用户并接收通知
- **深色模式**：内置主题切换器，支持浅色和深色模式
- **响应式设计**：移动优先的设计理念，同时支持桌面端和移动端导航
- **实时更新**：点赞、评论和关注的即时通知

## 技术栈

- **前端**：Next.js 14 与 React
- **样式**：Tailwind CSS 配合 shadcn/ui 组件
- **数据库**：由 neon 提供 PostgreSQL 搭配 Prisma ORM
- **认证**：Clerk
- **状态管理**：React Server Components + Client Components
- **图片上传**：uploadthing
- **部署**：Vercel

## 快速开始

1. 克隆仓库
2. 安装依赖：
   ```bash
   npm install
   ```

3. 配置环境变量：
   ```env
   DATABASE_URL="your_postgresql_database_url"
   NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY="your_clerk_publishable_key"
   CLERK_SECRET_KEY="your_clerk_secret_key"
   ```

4. 运行数据库迁移：
   ```bash
   npx prisma migrate dev
   ```

5. 启动开发服务器：
   ```bash
   npm run dev
   ```

6. 在浏览器中打开 [http://localhost:3000](http://localhost:3000)

## 项目结构

- `/src/app`：Next.js app router 页面和布局
- `/src/components`：可复用的 React 组件
- `/src/lib`：工具函数和共享代码
- `/prisma`：数据库模式和迁移文件
- `/public`：静态资源

## 功能详情

### 帖子
- 支持创建文字帖子，可选择附加图片
- 支持点赞和评论功能
- 响应式信息流展示
- 删除自己的帖子

### 用户资料
- 可自定义的个人资料信息
- 查看帖子和点赞内容
- 关注/取消关注其他用户
- 查看关注者和正在关注的数量

### 通知系统
- 实时通知功能，包括：
  - 帖子获得点赞
  - 帖子收到评论
  - 新的关注者

### 移动端支持
- 响应式设计
- 移动端优化导航
- 触摸友好的交互