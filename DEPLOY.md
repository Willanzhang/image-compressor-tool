# 📦 部署到 Vercel

## 方法一：通过 Vercel CLI（推荐）

### 1. 安装 Vercel CLI
```bash
npm install -g vercel
```

### 2. 登录 Vercel
```bash
vercel login
```

### 3. 部署项目
```bash
# 在项目根目录运行
vercel

# 或者直接部署到生产环境
vercel --prod
```

### 4. 配置域名（可选）
```bash
vercel domains add your-domain.com
vercel alias your-project-url.vercel.app your-domain.com
```

## 方法二：通过 GitHub 集成

### 1. 将代码推送到 GitHub
```bash
git init
git add .
git commit -m "Initial commit: 图片压缩工具"
git remote add origin https://github.com/yourusername/image-compressor-tool.git
git push -u origin main
```

### 2. 连接 Vercel
1. 访问 [vercel.com](https://vercel.com)
2. 点击 "Import Project"
3. 选择你的 GitHub 仓库
4. Vercel 会自动检测并部署

## 方法三：拖拽部署

1. 将项目文件夹打包成 ZIP
2. 访问 [vercel.com](https://vercel.com)
3. 直接拖拽 ZIP 文件到页面上
4. 等待自动部署完成

## 🔧 项目配置说明

项目已包含 `vercel.json` 配置文件，包含：

- **静态文件托管**：优化的静态资源服务
- **路由配置**：支持 SPA 路由
- **安全头**：基本的安全防护
- **缓存策略**：优化加载性能

## 🌍 访问地址

部署成功后，你将获得：
- 预览地址：`https://your-project-xxx.vercel.app`
- 生产地址：`https://your-project.vercel.app`

## ⚡ 自动部署

设置完成后，每次推送到 GitHub 主分支都会自动触发部署。

## 🛠️ 环境变量（如需要）

虽然本项目是纯前端应用，但如果后续需要添加环境变量：

```bash
vercel env add VARIABLE_NAME
```

## 📱 移动端测试

部署后在移动设备上测试：
1. 打开部署的网址
2. 测试拖拽上传功能
3. 验证响应式布局
4. 检查压缩功能性能

## 🚀 性能优化建议

- Vercel 自动启用 CDN 加速
- 静态资源自动压缩
- 支持 HTTP/2 和 Brotli 压缩
- 全球边缘节点分发

## 🔍 监控和分析

Vercel 提供：
- 访问统计
- 性能监控
- 错误追踪
- 部署日志