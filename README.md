# 图片压缩工具

一个纯前端的图片压缩工具，支持 JPEG/PNG/WebP/AVIF 的质量压缩与等比缩放。

## ✨ 特性

- 🎯 **纯本地处理** - 无需后端，所有处理均在浏览器中完成
- 📁 **拖拽上传** - 支持拖拽多张图片或点击选择
- ⚡ **批量处理** - 一次处理多张图片
- 🔧 **参数调节** - 支持质量(0-1)和最大尺寸限制
- 🖼️ **预览对比** - 显示压缩前后的效果对比
- 📊 **详细统计** - 显示文件大小、尺寸变化和压缩率
- 💾 **灵活下载** - 单张下载或批量打包ZIP
- 📱 **响应式设计** - 完美适配移动端和桌面端
- 🌓 **主题自适应** - 自动适配系统深色/浅色主题
- ⚡ **性能优化** - 大图使用Web Worker防止界面卡顿
- 🔄 **自动纠正** - 自动读取并纠正图片EXIF旋转信息

## 🚀 快速开始

### 直接使用

1. 下载 `index.html` 文件
2. 用现代浏览器（Chrome/Edge/Safari）打开即可使用

### 本地开发

```bash
# 克隆项目
git clone <repository-url>
cd image-compressor-tool

# 安装依赖（可选）
npm install

# 启动本地服务
npm run dev
```

### 在线使用

可以直接在 StackBlitz 中打开使用：

[![Open in StackBlitz](https://developer.stackblitz.com/img/open_in_stackblitz.svg)](https://stackblitz.com/github/your-repo/image-compressor-tool)

## 🎯 使用方法

1. **上传图片**：拖拽图片到上传区域或点击选择文件
2. **调整参数**：
   - 压缩质量：0.1-1.0（默认0.8）
   - 最大宽度：100-4000px（默认2000px）
   - 最大高度：100-4000px（默认2000px）
3. **压缩图片**：点击单张压缩或批量压缩
4. **下载结果**：单张下载或打包ZIP下载

## 🔧 技术实现

- **Canvas API** - 图片压缩和尺寸调整
- **Web Worker** - 大图片异步处理防止卡顿
- **FileReader API** - 文件读取
- **EXIF处理** - 自动纠正图片旋转
- **JSZip** - 批量下载ZIP打包
- **Drag & Drop API** - 拖拽上传
- **CSS Grid & Flexbox** - 响应式布局

## 📋 验收测试

项目已通过以下验收标准：

- ✅ 打开页面即可使用，无需安装
- ✅ 拖拽10张4000×3000的JPG图片
- ✅ 压缩到2000px、quality=0.8
- ✅ 页面无卡死现象
- ✅ 导出功能正常
- ✅ 显示原始/压缩后尺寸、体积与压缩率

## 🌟 浏览器支持

- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

## 📝 注意事项

- 所有图片处理均在本地完成，不会上传到任何服务器
- 默认会去除EXIF等元数据，但保留旋转信息用于自动纠正
- 大于5MB的图片会使用Web Worker处理以防止页面卡顿
- 支持的格式：JPEG、PNG、WebP、AVIF等浏览器原生支持的格式

## 📄 许可证

MIT License