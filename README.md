# AppleMusic_Sharing_Cards
生成卡片(图片)以分享Apple music上的专辑与音乐。Generate cards (images) to share albums and music on Apple Music.
在线使用Use it online：https://vnotheursansayoa.github.io/AppleMusic_Sharing_Cards/Applemusic_Cards.html
# 详细信息 Detailed Information

# 简体中文
一款纯前端、轻量级的单文件 HTML 小工具。适合用于社交平台的音乐分享。
解决了部分平台的Apple music中的音乐与专辑无法通过卡片分享的困扰。

## ✨ 核心特性

*    **双主题无缝切换**：内置 **白色主题 (Light)** 与 **暗黑主题 (Dark)**，适应不同风格的分享需求。
*    **丰富的排版与尺寸**：
    *   支持 **竖版 (Vertical)** 和 **横版 (Horizontal)** 两种基础布局。
    *   内置 8 种精调的尺寸比例（经典、瘦长、正方形、大号、宽幅、紧凑、社交）
*    **元数据抓取**：调用苹果官方 iTunes API
*    **自动生成专属二维码**：卡片底部内嵌对应链接的高清二维码，好友长按或扫码即可直达 Apple Music App 收听。

## 🛠️ 技术栈

*   **HTML5 / CSS3 (Flexbox)**：实现响应式、跨端一致的排版布局。
*   **Vanilla JavaScript (ES6+)**：核心逻辑控制。
*   **iTunes Search API**：用于根据分享链接中的 ID 获取歌曲公共元数据及高清封面图。
*   **[QRCode.js](https://github.com/davidshimjs/qrcodejs)** (通过 CDN 引入)：用于纯前端生成精准的二维码。
*   **[html2canvas](https://html2canvas.hertzen.com/)** (通过 CDN 引入)：用于将网页 DOM 元素高质量截图并转化为可下载的图像（支持跨域图像处理）。

## 💡 常见问题

**Q: 为什么获取不到歌曲信息？**
A: 请确保您输入的链接是完整的 Apple Music 分享链接。工具会自动识别链接中的国家代码（如 `/cn/`、`/us/`）以及歌曲 ID（`?i=xxxx`）。如果是一段无法解析的非官方链接则会报错。

**Q: 为什么导出的图片没有封面？（图片跨域问题）**
A: 这是由于浏览器严格的跨域安全策略（CORS）。本工具已经在 `html2canvas` 引擎中开启了 `useCORS: true`。如果在极少数网络环境下仍然无法加载封面，请尝试更换网络，或者直接使用手机自带的“截屏”功能截取预览区。

## 📜 许可协议

本项目仅供个人学习与日常分享使用，无任何商业用途。
Apple Music 相关图标、封面版权及数据均归属于 Apple Inc. 及相关唱片公司/艺术家所有。

# English
A pure frontend, lightweight single-file HTML tool. Perfect for sharing music on social platforms.
Solves the issue where certain platforms cannot share Apple Music songs and albums via cards.

## ✨ Core Features

*   **Seamless Dual Theme Switching**: Built-in **Light Theme** and **Dark Theme** to suit different sharing style needs.
*    **Rich Layouts and Sizes**:
*   Supports two fundamental layouts: **Vertical** and **Horizontal**.
*   Includes 8 finely-tuned size ratios (Classic, Tall, Square, Large, Wide, Compact, Social).
*    **Metadata Fetching**: Utilizes Apple's official iTunes API.
*    **Automatic QR Code Generation**: A high-definition QR code for the corresponding link is embedded at the bottom of the card. Friends can long-press or scan it to go directly to the Apple Music App and listen.

## 🛠️ Tech Stack

*   **HTML5 / CSS3 (Flexbox)**: For implementing responsive, cross-platform consistent layout and typography.
*   **Vanilla JavaScript (ES6+)**: For core logic control.
*   **iTunes Search API**: Used to fetch public song metadata and high-resolution cover art based on the ID from the share link.
*   **[QRCode.js](https://github.com/davidshimjs/qrcodejs)** (via CDN): For generating precise QR codes purely on the frontend.
*   **[html2canvas](https://html2canvas.hertzen.com/)** (via CDN): Used for high-quality screenshot capture of webpage DOM elements and conversion to downloadable images (supports cross-origin image processing).

## 💡 Frequently Asked Questions

**Q: Why can't I retrieve the song information?**
A: Please ensure the link you entered is a complete Apple Music share link. The tool automatically identifies the country code (e.g., `/cn/`, `/us/`) and the song ID (`?i=xxxx`) within the link. If it's an unofficial, non-parsable link, an error will occur.

**Q: Why is the exported image missing the cover art? (Cross-origin image issue)**
A: This is due to the browser's strict cross-origin security policy (CORS). This tool has already enabled `useCORS: true` in the `html2canvas` engine. If the cover still cannot be loaded in extremely rare network environments, please try switching networks or directly use the built-in "screenshot" function on your phone to capture the preview area.

## 📜 License Agreement

This project is for personal learning and daily sharing only, with no commercial use.
Apple Music-related icons, cover copyrights, and data are all owned by Apple Inc. and the respective record companies/artists.
