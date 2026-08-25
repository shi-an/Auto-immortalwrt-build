# ImmortalWrt XR30 / x86 自动编译

本仓库只保留两套 GitHub Actions 工作流：

- `build-pre.yml`：编译 MT7981 CMCC XR30 NAND 固件
- `build-x86.yml`：编译 ImmortalWrt x86/64 generic 固件

其他设备工作流、设备专用配置和源码更新检查工作流不在本仓库中。

## 使用方式

1. 在 GitHub Actions 中选择 `Build ImmortalWrt XR30` 或 `Build ImmortalWrt x86`。
2. 点击 `Run workflow`，按需选择插件开关。
3. 编译完成后，从 Actions artifacts 或 Releases 下载固件。

工作流会在运行时拉取对应的 ImmortalWrt 源码，不把源码目录或编译产物提交到本仓库。

## 配置文件

- `xr30.extra.config`：XR30 固件的追加配置
- `x86.extra.config`：x86/64 固件的追加配置
- `feeds.conf.default`：XR30 使用的 feeds 默认配置；x86 工作流会按自身配置生成 feeds

## 许可证

本仓库中的工作流和配置沿用所使用上游项目的许可证。
