# Pixel Code Dev 团队配置

这是 [Pixel Code Dev](https://github.com/Along-me/pixel-code-dev) 的独立公开配置仓库，不存放工具源码。

## 在工具中同步

右上角云朵按钮 → 团队配置同步：

```text
仓库：Along-me/pixel-code-config
分支：main
路径：shared/config.json
```

任何人都可以匿名拉取，无需 GitHub 账号。初始配置为空；维护者确认推送之后，团队成员才能拉取实际共享内容。

推送需要 GitHub Fine-grained Token：Repository access 选择 Only select repositories，只选择 `pixel-code-config`，Contents 权限为 Read and write。不要给 Token 授权工具源码仓库 `pixel-code-dev`，也不要使用包含其他仓库权限的 Classic Token。

共享 Token 只宜交给可信维护者：持有者仍可修改或删除本仓库配置，无法可靠区分每位操作者。撤销 Token 可收回权限；历史配置可以通过 GitHub 提交记录恢复。

## 数据范围

仅共享样式、样式分组顺序、变量、记忆、代码存档及其历史版本、自定义 Prompt。

禁止上传模型服务配置、模型列表、API Key、GitHub Token、聊天记录、个人界面配置和含密钥的本地备份文件。工具会在上传及下载时校验严格的共享字段白名单；不要在代码、变量或普通文本里粘贴任何凭据。公开提交的内容即使后来删除，也可能保留在 Git 历史和他人副本中。

共享协议为 `schemaVersion: 1`，单文件限制 900 KB。推送前先拉取并处理冲突；文件 SHA 校验防止过期内容覆盖他人更新。
