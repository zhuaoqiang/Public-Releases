# Changelog

## 2026-10-08 — Car-Collector 1.4.0 / 1040

完成：
- 发布 Tag `car-collector-v1.4.0`，包含 `collector-1040.apk` 与 SHA256 校验文件。
- `manifest/car-collector.json` 切换到 1.4.0 / 1040。
- 车机正式更新通道继续使用 `wj.bmpw.pw`。
- 云采集任务发布侧启用服务器统一全局发号、`request_id` 幂等和稳定 `task_id`；历史活动任务已归档清空。

验证：
- G run `37754125379`：72 tests / 0 failures / 0 errors / 0 skipped，Lint 0 error / 54 warnings，APK 签名、包名、1040 / 1.4.0 均通过。
- G run `37754996152`：服务器统一发号器与 GitHub 精确脚本 SHA256 一致；活动任务数 0，catalog revision 12，发号基线 current_sequence 29。
- G run `37755185203`：线上 `apps.json` 读回 1040 / 1.4.0，服务器端 APK SHA256 与候选包一致；按当前规则不重新下载整包公网 APK。
- G run `37755345417`：GitHub Release asset 元数据 SHA256 为 `98b090deb5284aec8d9b2521e6fab0d8ad3b7cf61c22be4e6fa55024caa28bc1`，大小 1,088,771 bytes。

## 2026-10-08 — Car-Collector 1.3.0 / 1030

完成：
- 发布 Tag `car-collector-v1.3.0`，包含 `collector-1030.apk` 与 SHA256 校验文件。
- `manifest/car-collector.json` 切换到 1.3.0 / 1030。
- 车机正式更新通道继续使用 `wj.bmpw.pw`。

验证：
- G run `37709509929`：线上 `apps.json` 读回 1030 / 1.3.0，服务器端 APK SHA256 与候选包一致；按当前规则不重新下载整包公网 APK。
- G run `37709624835`：GitHub Release asset 元数据 SHA256 为 `cfadec0edb236cf1c47c7a54002c8f78a65b48c7fb95826aff651166fc1c2b82`，大小 1,079,863 bytes。

## 2026-10-07 — Car-Collector 1.2.1 / 1021

完成：
- 发布 Tag car-collector-v1.2.1。
- GitHub Release 发布 collector-1021.apk 与 SHA256 校验文件。
- manifest/car-collector.json 已切换到 1.2.1 / 1021。
- 车机正式更新通道继续使用 wj.bmpw.pw；公共仓继续作为统一发布镜像和标准产品索引。

验证：
- G run 37556544971：Release 创建成功；APK asset 元数据 SHA256 为 0d931a7f790b273fe7d49c5238172987dd50c679177fb7b1a47e3786377af674，大小 1,074,607 bytes。
- 按当前发布规则未重新下载整包 APK；正式车机通道由 G run 37556407601 完成线上清单读回与服务器端 APK SHA256 校验。

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
