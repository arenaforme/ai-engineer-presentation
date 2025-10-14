# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是一个单页面 HTML 演示文稿项目,主题为"拥抱 AI 时代:从程序员到 AI 应用工程师的进化之路"。

## 技术栈

- **纯 HTML + CSS + JavaScript** - 无需构建工具
- **Tailwind CSS** (通过 CDN 引入)
- **Google Fonts** - Noto Sans SC 中文字体
- **原生 JavaScript** - 实现幻灯片切换和交互功能

## 文件结构

- `abc.html` - 主演示文稿文件,包含 31 张幻灯片
  - 完整的样式定义
  - 幻灯片内容(从封面到行动号召)
  - 交互逻辑(键盘导航、箭头按钮、进度条)

## 如何运行

直接在浏览器中打开 `abc.html` 文件即可查看演示:

```bash
open abc.html
```

或使用简单的 HTTP 服务器:

```bash
python3 -m http.server 8000
# 然后访问 http://localhost:8000/abc.html
```

## 幻灯片操作

- **下一张**: 点击右箭头、按空格键或右方向键
- **上一张**: 点击左箭头或左方向键
- **进度指示**: 底部进度条和页码显示

## 内容结构

演示文稿包含以下主题:
1. 封面和议程
2. AI 时代的机遇与挑战
3. 程序员角色的进化
4. FDE 工作模式(Fast, Direct, End-to-End)
5. AI 应用工程师的定义和能力
6. 公司转型计划
7. 转型路径和支持
8. 真实案例和行动号召

## 设计特点

- **深色主题** - 现代感强的黑色背景(#0a0a0a)
- **响应式布局** - 使用 clamp() 函数实现自适应字体大小
- **渐变动画** - 幻灯片切换时的淡入淡出效果
- **天蓝色高亮** - 使用 #0ea5e9 作为强调色
- **外部图片** - 通过 Unsplash CDN 引用背景图片

## 修改注意事项

- 修改幻灯片内容时,保持 `.slide` 类结构不变
- 添加新幻灯片需确保包含 `<div class="slide">` 和 `<div class="slide-content">` 结构
- 样式修改应在 `<style>` 标签内进行
- JavaScript 逻辑依赖于 `.slide` 类选择器,删除幻灯片后需测试导航功能

## 依赖项

所有外部依赖通过 CDN 加载:
- Tailwind CSS: `https://cdn.tailwindcss.com`
- Google Fonts: Noto Sans SC 字体族(300/400/500/700 字重)
- Unsplash 图片: 用于部分幻灯片的背景图

**注意**: 需要网络连接才能正确加载所有资源。中国大陆地区访问 Google Fonts 可能受限,建议考虑使用国内镜像或本地字体。
