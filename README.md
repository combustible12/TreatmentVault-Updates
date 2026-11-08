# HealthTrend 更新

HealthTrend 正式签名安装包与 update.json。手机通过应用内的一键更新检查、下载并校验新版。

## 发布签名版本

发布者将私有仓构建的原签名 APK 命名为 `HealthTrend-<versionCode>.apk`，与对应的 `publish.json` 一起提交到本分支。清单含 `versionCode`、`versionName` 和安装包的 `sha256`。也可以先在本仓以 `healthtrend-v<versionCode>` 为标签暂存名为 `HealthTrend.apk` 的 Release 附件，再提交 `publish.json`。暂存 Release 以本分支为目标，并关闭 latest 标记。

工作流核对包名、签名证书、版本及 SHA-256 后生成手机读取的 `update.json`。以工作流成功、匿名访问更新清单及 APK 均成功为发布完成条件。
