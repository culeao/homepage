# Litong Gong — Personal Homepage

简洁的英文静态学术主页，适合 GitHub Pages。纯 HTML / CSS，无 npm 依赖、无构建步骤、无第三方字体或追踪脚本。关闭 JavaScript 也能完整使用。

## 本地预览

直接打开 `index.html`，或在此目录运行：

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

浏览器访问 <http://127.0.0.1:8000>。

## 部署到 GitHub Pages

1. 在 GitHub 新建空仓库。若需要个人主页根域名，将仓库命名为 `你的用户名.github.io`；也可以使用普通仓库名（例如 `homepage`）。
2. 将本项目提交并推送到仓库。下方命令中的 `YOUR_USERNAME` 和 `YOUR_REPOSITORY` 需要替换：

   ```sh
   git add .
   git commit -m "Create personal academic homepage"
   git remote add origin https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
   git push -u origin main
   ```

3. 在仓库 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**，分支选择 `main`，目录选择 `/ (root)`，保存。
4. 等待 GitHub Pages 部署完成。个人仓库地址为 `https://你的用户名.github.io/`；普通仓库地址为 `https://你的用户名.github.io/仓库名/`。

资源使用相对路径，兼容这两种部署方式。`.nojekyll` 用于直接提供静态文件。本地已初始化 `main` 分支，但未提交。当前不绑定域名，也没有创建远程仓库或发布网站。部署步骤参考 [GitHub Pages 官方说明](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。

## 修改内容

- `index.html`：姓名、职称、单位、简介、论文、竞赛奖项和外部链接。复制一个 `.paper` 条目即可添加代表论文，其他论文放在 `.other-papers` 中；竞赛奖项放在 `.award-list` 中。
- `assets/style.css`：颜色、字体、留白、桌面和移动端布局。颜色变量集中在文件顶部。
- `assets/favicon.svg`：浏览器标签页图标。

如需添加照片、邮箱、GitHub 链接或简历，在简介区域加入真实信息即可。建议将照片、PDF 放入 `assets/` 并使用 `./assets/文件名` 相对链接。发布前也可以按个人偏好调整英文简介和代表论文顺序。

## 内容来源与维护

公开资料核对日期：**2026-11-03**。姓名、单位、研究方向及论文归属来自用户提供的 [Google Scholar](https://scholar.google.com/citations?user=09N7Ql0AAAAJ&hl=en)。原链接中重复的 `user` 参数已归一化。当前职称“阿里巴巴高级算法专家”（Senior Algorithm Expert）以及核心参与 HappyHorse 视频生成模型训练优化的经历由本人提供；其他研究主题根据下列论文概括。2022 年硕士毕业于中国科学院计算技术研究所的教育经历也由本人确认；不额外推断专业、导师、入学年份或学位授予单位。

竞赛部分根据本人提供的奖项截图整理，共 8 项。保留 2 项冠军、2 项第三名的名次与参赛规模；其余 4 项按本人要求统一展示为 **Bronze Award（铜奖）**，不展示原始第四名或第七名。日期与队内角色保留。中文赛事名称的英文为本站译名，非经核实的官方英文名称。

代表论文与展开列表分别按发表时间从新到旧排列，保留 6 篇代表论文与 9 篇其他论文的分组。同年论文参考正式版本上线时间或 arXiv 首次提交时间；同月预印本按 arXiv 编号倒序。代表论文顺序为：

1. [VC-VAE](https://link.springer.com/chapter/10.1007/978-3-032-37010-5_36)：ECCV 2026。
2. [TransVAE / Unifying CNNs and ViTs](https://link.springer.com/chapter/10.1007/978-3-032-37132-4_37)：ECCV 2026。
3. [RISE-T2V](https://arxiv.org/abs/2511.04317)：arXiv 预印本，2025。
4. [Taobao multimodal representations](https://arxiv.org/abs/2407.19467)：ACM CIKM 2024。
5. [AtomoVideo](https://arxiv.org/abs/2403.01800)：arXiv 预印本，2024。
6. [Hierarchical Masked 3D Diffusion](https://arxiv.org/abs/2309.02119)：ACM Multimedia 2023。

两篇 ECCV 论文的发表状态、完整作者名与摘要已通过 Springer 论文页及 [ECCV 2026 官方接收列表](https://eccv.ecva.net/Conferences/2026/AcceptedPapers) 核实；视频外扩论文的 ACM MM 2023 接收状态由其 arXiv 作者页面确认。其他论文保留在展开列表中，预印本仍明确标注为 arXiv preprint。

其他论文标题、作者缩写、年份和会议名称按 Scholar 展示整理。Scholar 中 VC-VAE 和视觉自编码器工作的无年份异名条目未重复列出，原始列表仍可通过 Scholar 查看。本页展示 15 个论文条目，其中 6 篇为代表论文，其余 9 篇可展开查看；并非自动同步的 Scholar 镜像。

没有固定展示易过时的引用量或 h-index。论文状态如有变化，请手动更新；页脚年份也为静态文本。
