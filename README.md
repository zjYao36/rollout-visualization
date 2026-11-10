# Rollout 数据可视化

图生、参考生各 10 组，每组 4 个 seed，共 80 条视频。

- 图生模型：`vidu34_img2video_20260912`
- 参考生模型：`vidu34_character2video_20261106`
- Seeds：`42`、`123`、`2026`、`3407`
- 同组使用相同条件、原始 prompt 和 PE caption，只改变 seed。

打开 `index.html` 可浏览全部 case，筛选模型、搜索文本、放大条件图、展开完整 PE，并同步播放四个 seed 的视频。

## GitHub Pages

将本目录推送到 GitHub 仓库后，打开 **Settings → Pages → Build and deployment**，
选择 **Deploy from a branch**、`main` 分支和 `/ (root)`，保存。
部署完成后，GitHub 会在同一页面给出可公开访问的网址。

所有视频、图片和缩略图均包含在仓库内，使用相对链接；页面不需要内网服务或 API。
`.nojekyll` 用于直接发布静态文件，无需安装或构建依赖。

每组目录包含 `conditions/`、`prompt.txt`、`pe.txt`、`config.json` 和四个 `seed_*.mp4`。
全部 80 条视频通过完整解码及参数核对；20 组内共 120 对 seed 的解码画面均不同。

发布说明：[GitHub Pages 文档](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

## 480p 对照测试

图生、参考生各 3 条，时长 12–16 秒，seed 42。复用原 case 的条件、prompt 和 PE，仅修改实际采样分辨率，原生生成 480 像素短边视频，未对视频进行缩放转码。
[查看 480p 对照](480p/)
