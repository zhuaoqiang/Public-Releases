# Public-Releases｜AI 接手规则

先读取 AiHub 当前 `AGENTS.md`、`任务索引.md` 和 `rules/docs.md`，再读本仓库 README、manifest 和当前 Release/Tag 状态。

## 项目定位
- 本仓库是 **公开下载/更新分发仓**，不是任何产品的源码仓。
- 每个产品使用自己的命名空间、Tag 和 `manifest/<product-id>.json`。
- 业务项目在其有效发布授权范围内可以更新**自己产品的** Release/Tag/assets/manifest；不能顺手改其他产品或共享发布规则。

## 公开边界
- 这个仓库是公开的。即使 owner 允许 AI 在私有环境保存密码/Token/私钥，这里仍然**禁止**上传任何真实凭据、私钥、内部配置、数据库、私有日志或受限制材料。
- 发布资产必须是 owner 明确允许公开的安装包、更新包、校验文件和公开说明。
- 私有签名材料只在私有项目仓库/受控环境使用，Public-Releases 只接收最终可公开产物。

## 发布完整性
- 客户端以自己的 manifest 为版本发现入口，不使用整个仓库的 `/releases/latest` 判断最新版。
- manifest 与对应 Release asset 必须保持版本、Tag、文件名、SHA256、兼容/更新信息一致。
- 发布完成要实际验证下载 URL 和 SHA256；“文件上传成功”不等于客户端更新链已经可用。
- 不删除历史 Release/Tag/manifest 兼容信息，除非 owner 明确要求并确认不会破坏旧客户端。

## 接班
发布任务可能跨会话。若某个产品发布尚未完成，任务状态主要写在该**业务项目**的 `AI-STATE.md`；本仓库根 `AI-STATE.md` 只记录共享仓自身结构/异常。新 AI 恢复发布前先核对产品私有仓库 commit、Release、asset、manifest 和实际下载，禁止重复创建版本。
