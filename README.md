\# Minecraft Server Downloader



一键下载所有正式版 Minecraft 服务器 JAR 文件  

A powerful desktop tool that lets you download any release version of the Minecraft server JAR with a single click.  

No more manual searching—just select, click, and your server core is ready.



\---



\## 核心特性 | Core Features



\- \*\*全版本覆盖\*\*：自动获取官方所有正式版列表，从早期版本到最新版均可下载  

&#x20; \*\*Full Version Coverage\*\*: Automatically fetches the complete list of official release versions, from early builds to the latest



\- \*\*现代化 GUI 界面\*\*：基于 PyQt6 的精美界面，支持深色 / 浅色主题切换，界面简洁直观  

&#x20; \*\*Modern GUI\*\*: Beautiful PyQt6-based interface with dark / light theme switching, clean and intuitive



\- \*\*多语言支持\*\*：内置中文和英文，可根据系统语言自动切换  

&#x20; \*\*Multi‑language Support\*\*: Built-in Chinese and English, with automatic switching based on system language



\- \*\*高性能下载\*\*：多线程设计，实时显示下载速度、进度和剩余时间，支持暂停 / 恢复 / 停止  

&#x20; \*\*High‑performance Download\*\*: Multi-threaded design with real‑time speed, progress, and remaining time display; supports pause, resume, and stop



\- \*\*智能管理\*\*：自动检测已下载文件，避免重复下载；磁盘空间预检查，防止空间不足  

&#x20; \*\*Smart Management\*\*: Automatically detects already downloaded files to avoid duplicates; disk space pre‑check prevents insufficient storage



\- \*\*便捷操作\*\*：版本搜索、全选 / 取消全选、一键开始，状态栏实时反馈  

&#x20; \*\*Convenient Operation\*\*: Version search, select all / deselect all, one‑click start, with real‑time status bar feedback



\- \*\*版本过滤\*\*：可筛选正式版、快照版、旧 Alpha/Beta 版，满足不同需求  

&#x20; \*\*Version Filtering\*\*: Filter release, snapshot, old alpha/beta versions to meet different needs



\- \*\*镜像源与自定义 API\*\*：支持切换官方 / BMCLAPI 镜像源，也可自定义版本清单 API 地址  

&#x20; \*\*Mirror \& Custom API\*\*: Switch between official and BMCLAPI mirrors, or specify a custom version manifest API URL



\- \*\*代理支持\*\*：HTTP / HTTPS 代理设置，方便内网或特殊网络环境  

&#x20; \*\*Proxy Support\*\*: HTTP/HTTPS proxy settings for corporate or restricted networks



\- \*\*跟随系统主题\*\*：自动识别系统暗色 / 明亮模式并同步界面风格（需安装 darkdetect 库）  

&#x20; \*\*Follow System Theme\*\*: Automatically detects system dark/light mode and syncs the UI (requires darkdetect library)



\---



\## 使用说明 | Usage Guide



\### 方式一：直接运行（Windows 用户推荐）

下载最新版本的 `MinecraftServerDownloader.exe`（单文件免安装），双击即可运行。  

\*\*Download the latest `MinecraftServerDownloader.exe` (portable, no installation required) and run it directly.\*\*



\### 方式二：从源码运行（Python 环境）

1\. 安装 Python 3.7 或以上版本  

2\. 安装依赖库：

&#x20;  ```bash

&#x20;  pip install pyqt6 requests darkdetect

&#x20;  ```

3\. 下载本项目源码并运行：

&#x20;  ```bash

&#x20;  python "Minecraft Server JAR files Download.py"

&#x20;  ```



\### 使用步骤 | Steps

1\. 选择或确认下载目录（默认为系统“下载”文件夹）  

&#x20;  \*\*Select or confirm the download directory (default is your system’s "Downloads" folder)\*\*

2\. 从版本列表中勾选需要下载的版本，也可使用搜索快速定位  

&#x20;  \*\*Check the versions you want from the list; use the search box to quickly locate a specific version\*\*

3\. （可选）设置并发下载数、代理、镜像源或自定义 API  

&#x20;  \*\*(Optional) Configure concurrent downloads, proxy, mirror, or custom API URL\*\*

4\. 点击“开始下载”，即可自动下载对应版本 JAR 文件  

&#x20;  \*\*Click "Start Download" and the corresponding JAR files will be downloaded automatically\*\*

5\. 下载完成后，JAR 文件会按版本号分组存放在子文件夹中，可直接用于启动服务器  

&#x20;  \*\*After download, JAR files are grouped in sub‑folders by version and can be used directly to launch your server\*\*



\---



\## 自行打包 | Build Your Own Executable



\### 使用 PyInstaller 打包为单文件 EXE

```bash

pip install pyinstaller

pyinstaller --onefile --windowed --name="MinecraftServerDownloader" --hidden-import=requests --hidden-import=darkdetect "Minecraft Server JAR files Download.py"

```

\- 打包成功后，在 `dist` 目录下可获得独立的 `.exe` 文件。

\- 如需添加图标，加入 `--icon=icon.ico` 参数。



\### 使用 Nuitka 打包（性能更优，推荐）

```bash

pip install nuitka

nuitka --standalone --onefile --windows-disable-console --plugin-enable=pyqt6 --include-package=requests --include-package=darkdetect --windows-icon-from-ico=icon.ico "Minecraft Server JAR files Download.py"

```

\- 需要安装 C 编译器（MinGW-w64 或 MSVC）。

\- 打包时间较长，但生成的 exe 启动更快、反编译难度更高。



\---



\## 项目贡献者 | Contributors



| 贡献者 (Contributor) | 贡献内容 (Contribution) |

|----------------------|------------------------|

| \[Minecraft-1314](https://github.com/Minecraft-1314) | 插件完整开发 (Complete plugin development) |



（欢迎提交 PR 加入贡献者列表）  

\*\*Welcome to submit PR to join the contributor list!\*\*



\---



\## 许可协议 | License



本项目采用 MIT 许可证，详情参见 \[LICENSE](LICENSE) 文件。  

\*\*This project is licensed under the MIT License, see the \[LICENSE](LICENSE) file for details.\*\*



\---



\## 支持我们 | Support Us



如果这个项目对您有帮助，欢迎点亮右上角的 Star ⭐ 支持我们，这将是对所有贡献者最大的鼓励！  

\*\*If this project is helpful to you, please feel free to star it in the upper right corner ⭐ to support us, which will be the greatest encouragement to all contributors!\*\*

