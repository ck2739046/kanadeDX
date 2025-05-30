---
title: 启动指南
description: 第一次设置游戏时的指南
---

## **1. 获取资源文件**

要获取游戏资源文件，你可以访问 [Telegram 群组](https://kdx.nightcord.com.de/zh/general/community) 或 [Discord 服务器](https://kdx.nightcord.com.de/zh/general/community) 的文件频道。本指南假设你已经获取了所需的文件。

---

## **2. 传输资源文件**

游戏资源文件是独立于游戏程序的。在下载包含游戏资源的种子文件后，请按照以下步骤操作：

### 方式 A：使用 Miniserve 传输

1. **在 `StreamingAssets` 目录中启动 miniserve**
    - **Windows**: 点击 `StreamingAssets/miniserve.exe` 并等待 3 秒。
    - **Mac**: 从 [GitHub Releases](https://github.com/svenstaro/miniserve/releases/tag/v0.29.0) 下载适合你的系统的文件：
        - 如果你使用的是 M 系列 CPU，请下载 `"aarch64-apple-darwin"` 版本。
        - 如果你使用的是 Intel CPU，请下载 `"x86_64-apple-darwin"` 版本。

        然后，将下载的文件复制到 `StreamingAssets` 目录，在该目录中打开终端，删除目录下的 .exe 文件，并输入：

      ```bash
      chmod +x ./miniserve* && ./miniserve* .
      ```

    - **Linux**: [你应该知道该怎么做 😉。](https://www.bilibili.com/video/BV1Nr4BeCEV9/)
2. **在游戏中输入下载地址**  
   该地址通常类似于 `http://192.168.1.123:8080`。你可以在 WiFi 设置中找到你的本地 IP 地址（这不是你的公网 IP，通常以 `192.168` 或 `10.0` 开头）。
3. **点击下载**。

> **注意**：如果 miniserve 显示多个 IP 地址，您需要在手机/平板浏览器中逐个尝试，直到找到正确的地址。通常只有一个 IP 地址是可用的。
>
> 如果所有 IP 地址都无法使用，可能是您的路由器防火墙阻止了连接，这在大学或公共网络中很常见。您可以尝试将手机/平板和电脑连接到移动热点或其他路由器。

### 方式 B：手动传输

请仅在无法使用 miniserve 的情况下使用该方式。注意通过 USB 2.0 协议进行的有线传输几乎总是比 miniserve 无线传输慢并可能需要数小时完成。

<details>
<summary>点击展开</summary>

1. 获取资源文件（有或没有 MovieData）

**Android**

2. 复制 StreamingAssets 文件夹到 `/sdcard/Android/data/app.KanadeDX/files/KanadeDX/`  
    有多种方法可以达到目的，速度各不相同：
    * USB MTP 文件传输：**非常慢**
    * `adb push` 命令：**快**（无进度条）
    * 在设备上下载种子：**快** (LibreTorrent/BiglyBT)
    * 先上传到云端再下载：**慢**
    * 传输 zip 文件并在设备上解压：**快**（需要双倍存储空间）
3. 在电脑上创建一个 .txt 文件并命名为 FinishedDownload，删除扩展名 ".txt"，并复制到游戏文件夹

**iOS**

2. 安装爱思助手
3. 安装驱动，该操作可在爱思助手内完成
4. 将设备连接至电脑，打开爱思助手并打开侧边栏“应用游戏”，找到 KanadeDX，再点击“浏览”
5. 拖拽文件夹
6. 在电脑上创建一个 .txt 文件并命名为 FinishedDownload，删除扩展名 ".txt"，并复制到游戏文件夹

</details>

## **3. 游戏设置**

你可以通过 **长按右上角的 ◀ 按钮** 来调整游戏设置。

### **延迟调整**

- 默认的输入延迟为 **+1 帧**，与官方街机相匹配。如果你发现自己的 LATE（延迟）判定比 EARLY（过早）判定更多，可以将其减少至 0。

### **网络设置**

- **KanadeDX** 默认连接到 **AquaDX 网络**。游戏构建版本中包含一个默认的 keychip，但使用该 keychip 注册的账户不会显示在排行榜上。
- 如果你想在排行榜上看到你的分数，请前往 [AquaDX 官网](https://aquadx.net/) 注册一个账号，并在 **“Setup Connection”**（设置连接）菜单中获取你的 keychip。
- 然后，在进入游戏前打开设置，替换默认 keychip 为你的专属 keychip。
- 最后，点击 **AIME 按钮** 扫描你的虚拟卡片，这将会在服务器上注册你的游戏档案。
