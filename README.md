# GKD Subscription Aggregator (GKD 订阅聚合仓库)

本项目是一个自动化的 **GKD (开屏广告跳过)** 订阅规则聚合仓库。它通过 GitHub Actions 定时从多个优质的上游订阅源同步最新的规则文件，为用户提供一个稳定、整合的订阅地址。

## 🌟 特性

- **🤖 全自动同步**: 每天北京时间早晨 **05:00** 自动拉取上游最新规则。
- **🔄 多源聚合**: 整合了社区中多个高质量的订阅源，避免单一源更新不及时的问题。
- **⚡ 实时可用**: 生成的 `.json5` 文件可直接用于 GKD 应用订阅。
- **🛡️ 冲突处理**: 内置自动重基 (Rebase) 机制，确保在并发更新时也能稳定推送。

## 📦 包含的订阅源

本仓库目前同步以下三个上游项目的规则：

| 文件名 | 来源项目 | 分支/路径 | 说明 |
| :--- | :--- | :--- | :--- |
| `aoguai_gkd.json5` | [aoguai/subscription](https://github.com/aoguai/subscription) | `custom/dist/aoguai_gkd.json5` | 傲乖订阅，规则丰富 |
| `ganlin_gkd.json5` | [ganlinte/GKD-subscription](https://github.com/ganlinte/GKD-subscription) | `main/dist/ganlin_gkd.json5` | 甘林订阅，更新频繁 |
| `MengNianxiaoyao_gkd.json5` | [MengNianxiaoyao/gkd-subscription](https://github.com/MengNianxiaoyao/gkd-subscription) | `main/dist/gkd.json5` | 梦年逍遥订阅 |
| `mrlctate_gkd.json5` | [mrlctate/gkd-mrlc](https://github.com/mrlctate/gkd-mrlc) | `main/dist/gkd.json5` | mrlctate 订阅 |

## ⚠️ 免责声明
本仓库仅作为规则搬运与聚合，所有订阅规则的版权和解释权归原作者所有。
本仓库不生产任何规则，不对规则的准确性、安全性或兼容性负责。
如果上游作者停止维护或要求删除，本仓库可能会同步移除相关规则。
使用 GKD 及本订阅源请遵守当地法律法规，仅供个人学习交流使用。

## 🙏 致谢
感谢以下开源项目作者提供的优质规则：
@aoguai
@ganlinte
@MengNianxiaoyao
GKD 官方项目
