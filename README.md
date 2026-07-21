# 凡岛大学 · 课程管理系统

学员端 + 管理端（身份切换）的课程学习与管理平台。

本仓库主文件为 course-management-system.zip：下载解压后即可本地运行。

## 功能概览

### 学员端
- 登录 / 首页统计与推荐课程
- 课程中心（搜索、分类、部门筛选、收藏、报名）
- 我的课程（进度、评价）
- 课程详情、消息通知、个人中心

### 管理端
- 管理概览（指标、报名趋势、最新动态）
- 课程管理（新增 / 编辑 / 查看 / 发布下架）
- 学员管理（搜索、部门筛选、详情）

## 技术栈

- 前端：Vue 3 + Vite + TypeScript + SCSS + Pinia + Vue Router
- 后端：Node.js + Express + Prisma + Zod + JWT
- 数据库：SQLite（本地零配置；生产可换 MySQL）

## 环境要求

- Node.js 18+（建议 20）
- npm

## 快速开始

### 1. 解压

解压 course-management-system.zip 后得到 course-client / course-server 等目录。

### 2. 启动后端

```bash
cd course-server
npm install
npx prisma db push
npm run db:seed
npm run dev
```

后端默认：http://localhost:8080

### 3. 启动前端

```bash
cd course-client
npm install
npm run dev
```

前端默认：http://localhost:5173
（已配置代理，/api 转到 8080）

## 演示账号

- lifengyun / 123456 ：部门管理员，可切换到管理端
- demo / 123456 ：普通学员

## 常用说明

- 首次运行务必先 db push 再 db:seed
- 详细设计见压缩包内设计文档

## License

仅供学习与实习演示使用。
