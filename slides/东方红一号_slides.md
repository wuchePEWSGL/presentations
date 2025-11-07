# 东方红一号 — PPT 源文件

本仓库包含为演示“东方红一号（中国第一颗人造地球卫星）”而准备的幻灯片文本与演讲稿原始文件，便于你在本地或在线生成正式 PPT。

文件结构建议：
- slides/东方红一号_slides.md  —— 幻灯片逐页要点与演讲备注
- slides/演讲稿.md           —— 口语化的完整演讲稿（约 8 分钟）
- images/IMAGE_SOURCES.md    —— 图片来源说明与建议
- images/  —— 放置下载的图片（校徽、卫星、发射照）
- 东方红一号_孙家栋_天津工业大学.pptx（可由本文件生成）

使用方法（两种）：
A) 在 GitHub 网页直接上传（最简单）
  1. 打开仓库页面，点击 “Add file” → “Upload files” 或 “Create new file”；
  2. 将 slides/*.md 和 images/IMAGE_SOURCES.md、README.md 逐一上传并 Commit 到 main；
  3. 在本地或在线下载图片放入 images/，然后在 PowerPoint 中复制粘贴或使用 Pandoc 生成 PPTX。

B) 在本地用 git（命令行）
  1. 克隆仓库：
     git clone https://github.com/wuchePEWSGL/presentations.git
     cd presentations
  2. 新建目录并保存文件（将上面文件保存到 slides/ 和 images/）；
  3. 提交并推送：
     git add .
     git commit -m "Add PPT source files: 东方红一号"
     git push origin main

用 Pandoc 自动生成 PPTX（可选）
1. 准备 template.pptx（可选，用于参考样式）和 images/ 下的图片（命名与 slides 中一致）。
2. 运行命令：
   pandoc slides/东方红一号_slides.md -o 东方红一号_孙家栋_天津工业大学.pptx --resource-path=images --reference-doc=template.pptx

备注：
- 请务必使用公开来源的图片并在备注中保留原始署名与来源信息。
- 校徽的使用请遵循天津工业大学的标识使用规范（你已授权在本展示中使用校徽）。
