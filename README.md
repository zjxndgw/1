# 人人互助平台一体化部署说明

## 文件结构
backend/              # 后端 Node.js + 前端静态文件
  ├─ index.js          # 后端 + 静态文件入口
  ├─ package.json
  ├─ .env              # 管理员助记词
  └─ dist/             # React 前端打包文件

## 部署步骤

1. 安装依赖
```bash
cd backend
npm install
```

2. 启动服务（测试用）
```bash
node index.js
```
- 访问 http://localhost:3000
- 前端页面和 API 接口都在同一域名下

3. 云端部署（Render/Railway/Vercel）
- 直接部署 backend 文件夹即可
- dist/ 文件夹包含前端打包文件
- 不需要单独配置 VITE_API_URL

4. 管理员登录
- 访问 /admin/login
- 输入 12 个助记词登录后台
