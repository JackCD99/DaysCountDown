<div align="center">
  <img src="assets/app-icon.png" width="132" height="132" alt="Days Count Down 应用图标">
  <h1>Days Count Down</h1>
  <p><strong>把重要时间稳稳放在桌面上。</strong></p>
  <p>简洁、自然的桌面倒计时、定时计划与 AI 学术会议 Deadline 小组件。</p>

  [![Version](https://img.shields.io/badge/version-v1.2.0-3478D4?style=flat-square)](https://github.com/JackCD99/DaysCountDown/releases/tag/v1.2.0)
  ![Windows](https://img.shields.io/badge/Windows-10%2F11-0078D4?style=flat-square&logo=windows11)
  ![macOS](https://img.shields.io/badge/macOS-Intel%20%7C%20Apple%20Silicon-111111?style=flat-square&logo=apple)
  ![License](https://img.shields.io/badge/license-Proprietary-lightgrey?style=flat-square)
</div>

> [!IMPORTANT]
> 本仓库目前仅用于发布软件安装包与使用文档，**暂不公开源代码**。请从右侧 Releases 或下方链接下载，不要从第三方站点获取。

## 下载

前往 [v1.2.0 Release](https://github.com/JackCD99/DaysCountDown/releases/tag/v1.2.0)：

| 平台 | 文件 | 适用设备 |
| --- | --- | --- |
| Windows x64 | `DaysCountDown-Setup-1.2.0-x64.exe` | Windows 10 1809 及以上、Windows 11 |
| macOS Apple Silicon | `DaysCountDown-1.2.0-macOS-arm64-unsigned.app.zip` | M1 / M2 / M3 / M4 等 Apple 芯片 Mac |
| macOS Intel | `DaysCountDown-1.2.0-macOS-x64-unsigned.app.zip` | Intel 芯片 Mac |

## 主要功能

- **桌面倒计时**：精确到秒，标题与剩余天数随窗口自适应缩放，避免内容截断。
- **多卡片布局**：倒计时与会议共享 1–10 张卡片额度，可通过右键拖动平滑调整顺序。
- **定时计划**：支持今日计划与普通计划，包含到期提醒、完成、延后、调整和删除。
- **AI 会议 Deadline**：自动读取 CCFDDL 数据，支持 AAAI、MM、CVPR、ICML、ICLR、NeurIPS、MICCAI、ICCV、ECCV、WWW 等会议。
- **首次启动即用**：首次运行会自动更新会议数据，并在显示上限内直接展示所有默认选中的有效会议。
- **北京时间**：会议 Deadline 统一转换为北京时间；可查看会议时间、地点与官方网站。
- **视觉定制**：20 组协调配色、整体透明度、毛玻璃效果及紧凑布局。
- **桌面驻留**：支持锁定、隐藏到屏幕边缘、托盘快捷操作和开机自动运行。
- **多显示器适配**：针对不同 DPI 与大小的显示器处理窗口迁移和重新渲染。

## 安装

### Windows

1. 下载 `DaysCountDown-Setup-1.2.0-x64.exe`。
2. 双击安装，可选择创建桌面快捷方式和开机自动运行。
3. 当前安装包尚未使用商业 Authenticode 证书签名；若 Windows 显示 SmartScreen 提示，请确认文件来自本仓库并核对 SHA256 后再运行。

### macOS

1. 根据芯片选择 `arm64` 或 `x64` 压缩包。
2. 解压后，将 `Days Count Down.app` 拖入“应用程序”。
3. 当前构建尚未完成 Apple Developer ID 签名与公证。首次打开被拦截时，请前往“系统设置 → 隐私与安全性”，确认来源后选择“仍要打开”。

更完整说明见 [macOS 安装说明](docs/macOS安装说明.md)。

## 会议数据逻辑

- 数据来自 [CCFDDL](https://ccfddl.top/) 的公开会议数据仓库。
- 只展示当前年份或下一年份、仍有有效 Deadline 的会议届次。
- 最近有效节点优先展示，顺序为注册、摘要、全文、补充材料。
- 首次运行自动刷新；后续采用本地缓存和周期更新，网络失败不会打断倒计时主功能。
- 设置中的会议圆点用于控制显示与隐藏，会议卡片与手动倒计时共用显示上限。

## 数据与隐私

- 倒计时、计划、窗口位置和偏好设置保存在本机，不上传到开发者服务器。
- 应用仅在更新会议数据时访问 GitHub 上的 CCFDDL 数据源；点击“打开会议官网”时才会打开对应外部网页。
- 发布包不包含开发者设备上的倒计时、计划、会议缓存、日志或测试数据。

## 文件校验

| 文件 | SHA256 |
| --- | --- |
| `DaysCountDown-Setup-1.2.0-x64.exe` | `7ED1F78EDABBB561B9CAF272DB6E50E9A28FE18B218E506008A79896F48D7840` |
| `DaysCountDown-1.2.0-macOS-arm64-unsigned.app.zip` | `E54CEE6AA92DE3C8C389970EE2994C3A942F8608957B530C5F0806E2A0C6F8AA` |
| `DaysCountDown-1.2.0-macOS-x64-unsigned.app.zip` | `0C04ACDE330BBDE42B44134D779D7CB1EA375EC810FEFB5F8455FD72194004FC` |

三个发布文件在上传前均已使用 Windows Defender 扫描，未发现威胁。

## 反馈

- Bug 与功能建议：请使用 [GitHub Issues](https://github.com/JackCD99/DaysCountDown/issues)
- 联系邮箱：`873728473@qq.com`

提交问题时，建议附上操作系统版本、应用版本、显示器缩放比例、复现步骤和截图。请勿上传包含个人计划内容的配置文件。

## 版权

Copyright © 2026 Hyu. All rights reserved.

本软件为闭源软件；仓库公开不代表源代码开源。详情见 [版权与使用许可](LICENSE.md)。

