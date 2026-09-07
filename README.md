# FreeView TV — Releases

Android TV 客户端的安装包与更新清单。源码在私有仓库，这里只放发布产物。

- `latest.json`：电视端「检查更新」读取的清单（见下）
- 每个版本的 APK 挂在 [Releases](../../releases) 里，tag 为 `tv-v<versionName>`

## 安装

```bash
adb connect <电视IP>:5555
adb install -r FreeView-TV-<version>.apk
```

## latest.json 格式

```json
{
  "versionCode": 1,
  "versionName": "0.1.0",
  "minApiVersion": 1,
  "apkUrl": "https://github.com/woaimidi/freeview-releases/releases/download/tv-v0.1.0/FreeView-TV-0.1.0.apk",
  "notes": "首个版本"
}
```

电视端比较 `versionCode`，大于自身则提示更新并给出 `apkUrl`；`minApiVersion` 用来提示服务端是否需要升级。
