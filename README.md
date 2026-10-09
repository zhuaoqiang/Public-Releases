# 公共发布仓

这是统一的公开安装包、更新包和校验文件发布仓。

各业务项目的源码继续保存在各自的私有仓库中；本仓库只保存明确允许公开下载的发布资产，不保存业务源码、Token、私钥、内部配置、数据库或其他非公开资料。

## 发布约定

- 每个产品使用独立的产品 ID 和 Tag 命名空间，例如 `easylink-windows-v1.0.0.5`、`fnos-cf-v0.3.7`。
- 每个产品使用自己的版本索引：`manifest/<product-id>.json`。
- 客户端只读取自己产品的 manifest，不使用整个仓库的 `/releases/latest` 判断产品最新版。
- 安装包、更新包等二进制文件通过 GitHub Release assets 发布。
- manifest 记录当前版本、对应 Tag/Release、资产名称、SHA256、发布时间以及必要的更新和兼容信息。
- 客户端下载后应校验 manifest 中登记的 SHA256。
- 新项目需要公开分发安装包或更新包时，默认复用本仓库并增加自己的产品命名空间和 manifest。

## 当前产品

- fnOS-CF：`manifest/fnos-cf.json`
- EasyLink Windows：`manifest/easylink-windows.json`
- Car-Collector（历史/兼容清单）：`manifest/car-collector.json`
- 车机采集助手：`manifest/car-factory-helper.json`
- DiPlay Android 8.1：`manifest/diplay-android81.json`

## 维护原则

本仓库是公开分发入口，不是源码维护仓。发布前必须确认文件允许公开；任何凭据、内部数据和私有项目材料都不得上传。
