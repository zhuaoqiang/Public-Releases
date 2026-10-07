# Changelog

## 2026-10-07 — Car-Collector 1.2.0 / 1020

完成：
- 发布 Tag `car-collector-v1.2.0`。
- GitHub Release 发布 `collector-1020.apk` 与 SHA256 校验文件。
- `manifest/car-collector.json` 已切换到 1.2.0 / 1020，并记录源码提交与现有车机更新通道。
- 车机正式更新通道继续使用 `wj.bmpw.pw`，公共仓作为统一发布镜像和标准产品索引。

验证：
- AI-PC-Bridge G run `37554531263`：Release 创建成功并重新下载资产校验。
- APK SHA256：`69cc6b5b4347e78ac12d392ebe531d2db2246e2a2c3b28e919ec0f948cef96db`。

## 2026-10-06 — Car-Collector 1.1.9 / 1019

完成：
- 新增产品命名空间 `car-collector`，Tag `car-collector-v1.1.9`。
- GitHub Release 发布 `collector-1019.apk` 与 SHA256 校验文件。
- 新增 `manifest/car-collector.json`，记录版本、资产、SHA256、发布时间、源码提交与现有车机更新通道。
- 车机正式更新通道仍使用 `wj.bmpw.pw`，本仓作为统一公共发布镜像与标准产品索引，不改变现有客户端地址。

验证：
- AI-PC-Bridge G run `37475101949`：Release 创建成功并重新下载资产校验。
- APK SHA256：`02e42073e0cd9af02d71ff02c39ad323fbbd5d8d99985f117f4095312b3ab0bc`。

## 2026-10-05 — 统一公共发布仓定位收口

完成：
- `zhuaoqiang/Public-Releases` 已作为跨项目统一公共发布仓维护；业务源码仍留在各自私有仓。
- GitHub Description 已从旧的 EasyLink 专用英文说明改为：`统一公开发布安装包、更新包和校验文件；各项目源码在私有仓库维护`。
- 已确认 EasyLink Windows `1.0.1.0` 与 fnOS-CF `0.3.9` 的产品独立 manifest 继续存在；本批次未改产品 Release 资产或版本索引。
- 仓库继续使用产品命名空间 Tag 与 `manifest/<product-id>.json`，不把全仓 `releases/latest` 当作各产品最新版权威。

验证：
- AI-PC-Bridge G run `37252224336`：`success`。
- Runner 日志：`PUBLIC_RELEASES_DESCRIPTION_OK=True`、`G_TASK_OK=True`。
- GitHub 仓库元数据读回确认 Description 与中央标准完全一致。
