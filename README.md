# UnityShutdownFix

修复 Unity 退出时辅助功能清理过程中的问题。

支持 Windows x64、Beat Saber **1.45.2_28848**，依赖环境包含本地移植的模组；其他依赖组合的兼容性需另行确认。仅适用于 SHA256 为 `826f0d671c0d3d7c852c32051a6ebd6a3d715d27e5323a5e34dbb33eef407fdd` 的 `UnityPlayer.dll`。

## 安装

从 [Releases](https://github.com/StarsWhere/UnityShutdownFix/releases) 下载压缩包，关闭游戏后将包内目录合并到游戏根目录。所需依赖及版本见 [manifest](scripts/unity_shutdown_fix/UnityShutdownFix.manifest.json)。

## 构建

准备 PowerShell 7 和已安装兼容依赖的游戏，在 PowerShell 中运行：

```powershell
git clone https://github.com/StarsWhere/UnityShutdownFix
cd UnityShutdownFix
pwsh -File scripts/build_release.ps1 -GameRoot 'C:\Games\Beat Saber'
```

临时文件位于 `.tmp/`，发布文件位于 `releases/`。

## 许可

[MIT](LICENSE)，第三方声明见 [THIRD-PARTY-NOTICES.txt](THIRD-PARTY-NOTICES.txt)。
