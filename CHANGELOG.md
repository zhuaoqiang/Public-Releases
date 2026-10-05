# Changelog

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
