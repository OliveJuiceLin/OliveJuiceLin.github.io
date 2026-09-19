# 更新 PDF 简历指南

本仓库的顶部 **CV** 菜单链接到 `files/` 目录中的 PDF。为避免每次更新时遗漏配置，今后请固定使用文件名：

```text
files/Yilin_Wang_CV.pdf
```

## 日常更新（推荐做法）

1. 准备好新版 PDF，并命名为 `Yilin_Wang_CV.pdf`。
2. 在 GitHub 网页中进入 `files/`，上传同名文件并选择覆盖已有文件；或在本地直接替换该文件。
3. 提交（commit）后，打开 `Actions`，确认最新的 `pages build and deployment` 显示绿色的 **Success**。
4. 用无痕窗口打开：<https://olivejuicelin.github.io/files/Yilin_Wang_CV.pdf>，确认下载到的是新版本。

只要文件名保持不变，顶部菜单和别人保存的简历链接都不需要再修改。

## 第一次需要修复的配置

目前菜单仍指向已删除的旧文件。请在 `_data/navigation.yml` 中将：

```yml
url: /files/wyl-cv-en-v4.pdf
```

改为：

```yml
url: /files/Yilin_Wang_CV.pdf
```

提交并等待 Actions 成功后，点击网站顶部的 **CV** 菜单确认不会出现 404。

## 如果必须改 PDF 文件名

除了上传新文件外，还必须同步修改 `_data/navigation.yml` 里 CV 条目的 `url`，使其与 `files/` 下的文件名（含大小写）完全一致。GitHub Pages 的路径区分大小写；例如 `Yilin_Wang_CV.pdf` 与 `yilin_wang_cv.pdf` 是不同地址。

确认新链接正常后，再删除旧 PDF，避免网站在更新过程中出现失效链接。

## 不需要为 PDF 简历更新的文件

- `_config.yml`：全站资料和搜索引擎信息，不保存 PDF 路径。
- `_pages/cv.md`、`_pages/cv-json.md`：目前没有被顶部菜单使用；它们是另一套网页简历模板。除非未来要启用 `/cv/` 或 `/cv-json/`，否则不必修改。

## 最短检查清单

- [ ] `files/Yilin_Wang_CV.pdf` 已替换为最新版本。
- [ ] `_data/navigation.yml` 的 CV 链接仍为 `/files/Yilin_Wang_CV.pdf`。
- [ ] GitHub Actions 的 Pages 部署成功。
- [ ] 网页顶部 CV 菜单和 PDF 直链均可打开。
