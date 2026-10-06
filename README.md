解决麻烦的工具盒  / Problem-Solving Toolbox
一个无需安装、点开即用的本地 HTML 网页工具箱
A local HTML toolbox that requires no installation and is ready to use.
5.0新增了代码编辑功能，并且3D模块大更新，你可以编辑模型了，并且优化了移动端适配
4.0新增了播放器的功能，有自动添加封面的功能，可以像图书馆那样轻松浏览你文件夹里面不同格式的文件（方向键翻页，视频，图片，PDF等等可以同时进行不用转换其他播放器），转换器支持多文件夹导入并且转换后生成多压缩包导出，并且修复了3D文件无法导入的bug。（导入文件请点击按钮导入，拖拽导入功能还在弄）
⚠️ 安全注意：由于最近旧版 ffmpeg 解码器漏洞与ChromeV8引擎越界写入漏洞（2026年6月爆出的严重浏览器漏洞）我更新了防护升级版本，不过由于攻击为极小概率事件，所以保留原始版本，没有更新浏览器的用户可以下载旧版，不过安全风险要需知。我已经尽力更新了网页程序避免被漏洞利用，但是真正有效的防护在于自己，请不要乱下东西
以下为应对策略：1版本强制:本地桥启动前自动跑 ffmpeg -version低于 7.1.3 直接拒绝启动    2编码器白名单：防护升级版只允许 libx264/libx265/libvpx/... 等已知安全编码器，其余一律拒绝。   3畸形文件拦截 + 体积上限：输入体积硬上限 2GB（转码）/1GB（字幕）
4下载界面安全须知：在"本地 GPU 工具包"对话框加了醒目红色安全区块，告知用户必须用官方源、保持 ffmpeg ≥7.1.3、勿处理来源不明媒体。
5浏览器内核自检:启动时检测 Chromium 内核版本，低于 140（覆盖上述在野零日修复基线）即弹出顶部红色安全警告浮层，明确列出在野 CVE 编号，并给"前往升级"按钮。
6安全响应:HTML头加了X-Content-Type-Options:nosniff以及监控型CSP


核心功能 (Core Features)
5.0新增代码编辑功能
<img width="2541" height="1397" alt="屏幕截图 2026-10-07 004734" src="https://github.com/user-attachments/assets/50f07481-05a6-4ecb-a293-199aaa7ee12c" />

4.0新增播放器功能，有自动封面功能，你可以像图书馆那样预览你的文件。支持图片，视频，表格，代码等等大部分格式（包括avif之类的）。
<img width="2510" height="1392" alt="屏幕截图 2026-10-06 001921" src="https://github.com/user-attachments/assets/56dd4dfc-3fd9-4781-9127-d5547acbedc5" />

1绘画功能 (Drawing)
<img width="1280" height="708" alt="demo2" src="https://github.com/user-attachments/assets/d4a4534a-ba0e-4687-a816-6c5bd5214b64" />
笔刷导入：支持导入 PS (Photoshop) 和 SAI 的笔刷文件。

(Brush Import: Supports importing brushes from PS and SAI.)

格式导出：支持将作品导出为 PSD 或 PNG 格式。

(Export: Save your work as PSD or PNG files.)

2图片编辑功能（Image Editing）
<img width="2557" height="1418" alt="demo3" src="https://github.com/user-attachments/assets/ec367b10-4092-42df-baf8-9e84237a640c" />
基础编辑：具备调色、滤镜、锐度、对比度调整等功能，操作类似手机修图软件。

(Basic Editing: Adjust color, filters, sharpness, and contrast, similar to mobile photo editors.)

3视频处理与 AI 字幕 (Video Processing & AI Subtitles)
<img width="2550" height="1401" alt="demo4" src="https://github.com/user-attachments/assets/285b6b1d-434b-4028-849f-bcf8b33d8539" />
3.1AI 字幕识别：内置 AI 字幕功能。(AI Subtitle Recognition: Built-in AI-powered subtitle generation.)
<img width="1280" height="700" alt="demo4 1" src="https://github.com/user-attachments/assets/c5cf7d76-25b6-45ba-b1cb-b5f6d16ab2c2" />
注意: 受限于网页性能，建议单次识别时长控制在 30秒以内，避免一次性上传过长视频导致网页崩溃或识别精度下降。

Note: Due to browser limitations, it is recommended to process videos in clips of under 30 seconds. Long videos may crash the page or reduce accuracy.

3.2显卡加速：提供本地显卡加速选项（需自行配置环境，不适合小白用户）。

(GPU Acceleration: Option for local GPU acceleration is available but requires manual environment configuration.)

4文档处理 (Document Processing)
<img width="2559" height="1401" alt="demo5" src="https://github.com/user-attachments/assets/8e6d4964-feea-4aee-8ef8-a091ad2de15b" />
格式互转：支持 PDF 与 Word 互转，以及 PDF 转 PPT、Word 转表格。

(Format Conversion: Convert between PDF & Word, PDF to PPT, Word to Excel sheets.)

4.1文档转图片：支持将上述文档格式转换为图片。

(Doc to Image: Convert documents into image formats.)

5多媒体转换 (Media Conversion)
<img width="2559" height="1407" alt="demo6" src="https://github.com/user-attachments/assets/d9c4782c-a210-4d67-a885-e40d9d21a37b" />

格式转换：支持视频与图片格式的相互转换（例如将小众的 AVI 格式转为通用的 PNG/JPG）。

(Conversion: Transform between video and image formats, e.g., AVI to PNG/JPG.)

兼容性提示：部分浏览器可能无法解码某些小众格式，已尽力适配但仍有兼容性问题。

(Compatibility: Some niche formats may not be supported by all browsers due to decoding limitations.)

6三维预览：支持三维模型文件预览和简单编辑。(3D Preview: Preview 3D model files.)
<img width="2518" height="1391" alt="屏幕截图 2026-10-07 000516" src="https://github.com/user-attachments/assets/0a45eb82-7d12-4d6e-bd12-ff2b513e6efa" />

7在线/本地翻译：提供可选的在线或本地翻译功能。(Translation: Optional online or local translation feature.)
<img width="2558" height="1398" alt="demo8" src="https://github.com/user-attachments/assets/647733c7-27e8-4751-9915-8429522cc1c9" />

8调色功能(Color Adjustment Feature)
<img width="2550" height="1397" alt="demo10" src="https://github.com/user-attachments/assets/34077166-f9c7-47ae-9710-3f9b99cda062" />
适合临时轻量调色，适用于没下载软件或者懒得开的
Suitable for temporary and lightweight color correction. It is applicable for those who haven't downloaded the software or are too lazy to open it.

 快速开始 (Quick Start)
下载仓库中的  解决麻烦的工具盒.html  文件。
(Download the  解决麻烦的工具盒.html  file from the repository.)

直接在本地使用浏览器（如 Chrome、Edge）打开该 HTML 文件即可开始使用。
(Simply open the HTML file with a local browser (e.g., Chrome, Edge) to start using.)
如果html下载失败，可以将txt文件后缀名改为html即可正常使用(If the HTML download fails, you can simply change the file extension of the TXT file to HTML and it will work properly.)
 
 重要提示 (Important Notes)

数据保存：本工具为网页形式，1.0版本不具备实时自动保存功能。退出网页后数据将会丢失，请在操作过程中（尤其是处理大文件时）务必及时导出并保存！2.0具有该功能。⚠️ 一个使用提醒：直接双击用file://打开时，浏览器安全策略可能不让弹出"选择文件夹"。此时自动保存会落到"浏览器本地缓存"（开始页有恢复下载入口，不会丢）要真正写入你指定的文件夹建议用最新 Chrome/Edge，并通过本工具的本地桥或本地服务器(http://localhost)打开页面，另外自动保存设置仅在开始页配置，点"开始绘画"前请先启用并选好保存地址与格式。
(Data Saving: This is a web-based tool and does NOT have real-time auto-save. Data will be lost upon closing the tab. Please export your work manually during the process, especially for large files!)

环境配置：部分高级功能（如本地显卡加速）需要用户具备一定的技术基础来配置运行环境。


一下是历史更新记录
(Environment Setup: Advanced features like local GPU acceleration require technical knowledge to set up.)
2.0添加了自动保存功能，并且在文档内添加了繁体与简体互换功能，增加txt导出，在转换器内添加文档转换，可以批量进行繁体与简体的互换操作
Version 2.0 introduces an auto-save feature, adds the ability to switch between traditional and simplified Chinese within documents, supports TXT export, and includes document conversion in the converter, enabling batch operations for converting between traditional and simplified Chinese.
3.0增加了检测功能（截屏功能因为浏览器的安全限制没弄起来，作者本人懒得删了）
3.0 added detection functionality (screenshot feature was not implemented due to browser security restrictions, and the author was too lazy to remove it)
