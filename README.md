<div align="center">

# NCE Flow

Tap any sentence, keep reading.  
简约 · 高效 · 专注的新概念英语在线点读（NCE1–NCE4）。

</div>

## ✨ 特性

- 句子级点读：点击任一句，从该句开始连续播放，自动高亮并居中
- 语言视图：EN / EN+CN / CN 三态切换（持久化保存）
- 现代 UI：Apple 风格、浅深色自适应、顺滑过渡
- 零依赖：纯静态 HTML/CSS/JS，可直接 GitHub Pages 部署
- LRC 兼容：支持 `英文|中文` 同行，或“同时间戳上下两行”堆叠格式
- 批量翻译：内置 `translate_lrc.py`，可将纯英文 LRC 转双语（可原地写回）

## 🗂 目录结构

```
assets/          # 样式与脚本（styles.css, app.js, lesson.js）
index.html       # 首页（书目 + 课程列表）
lesson.html      # 课文点读页
static/data.json # 书目与课程元数据
NCE1..NCE4/      # 音频与 LRC 资源（文件名与 data.json 一致）
```

## ⬇️ 获取完整代码

请通过下述任一方式获取项目，以确保音频（mp3）完整：

- 推荐：`git clone https://github.com/luzhenhua/NCE-Flow.git`
- 或从 Releases 页面下载打包好的压缩包（含完整音频）：https://github.com/luzhenhua/NCE-Flow/releases

注意：不要使用 GitHub 页面右上角的 “Code → Download ZIP”。该 ZIP 可能不包含完整的 mp3（或仅为指针文件），会导致页面无声音。

## 🚀 本地运行

建议使用本地静态服务器（避免浏览器对 file:// 的 fetch 限制）：

```
python3 -m http.server 8080
# 访问 http://localhost:8080
```

或直接将仓库部署到 GitHub Pages（默认入口为根目录的 `index.html`）。

## 🌐 演示与部署

- 演示站托管：部署在 腾讯云 EdgeOne（静态托管）。
- 项目为纯静态站点，理论上支持任意静态平台：Vercel、Cloudflare Pages、GitHub Pages 等。
- 部署要点：确保静态资源完整上传（尤其是 `NCE1..NCE4/` 下的 mp3 与 lrc），入口指向 `index.html`。

## 🎧 LRC 规范（本项目兼容两种）

1) 同行双语（推荐）

```
[mm:ss.xx]English sentence | 中文译文
```

2) 上下两行（同时间戳）

```
[mm:ss.xx]English sentence
[mm:ss.xx]中文译文
```

> 播放端自动识别两种格式；连续播放的分段时长会自动兜底（避免极短句抖动）。


## 🙏 致谢

- 原项目与灵感来源：[iChochy/NCE](https://github.com/iChochy/NCE)

  在此对原作者和社区表达感谢。

- 首页整合书目与课程列表；
- 课文页支持 EN/EN+CN/CN 三态语言视图；
- 句子级点读 + 连续播放；
- 视觉与动效统一（浅/深色自适应）。

- 感谢贡献：
  - https://github.com/reaishijie 提交的 PR（播放速度控制与持久化）：
    https://github.com/luzhenhua/NCE-Flow/pull/3

## 📄 协议

本仓库代码遵循仓库内 LICENSE 文件所述协议。音频与文本内容版权归原权利人所有，仅用于学习研究，请勿转载或商用。

---

如有侵权，请联系：openai.luzhenhua@gmail.com，我们将尽快处理。
