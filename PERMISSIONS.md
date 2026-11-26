# 浏览器权限说明
当前 Manifest V3，Chrome 116+；未改变 IV.4 的权限。保留跨站素材发现能力，并向用户透明说明。

| 权限 | 用途/边界 |
|---|---|
| activeTab | 保留当前标签页授权兼容；当前静态审计未证明它必不可少 |
| scripting | 网页脚本注入与适配 |
| downloads | 创建/查询/控制浏览器下载 |
| storage | 本地设置、诊断及旧数据迁移 |
| webRequest | 观察特定媒体请求，用于适配 |
| webNavigation | 核对网页及框架身份、导航恢复 |
| offscreen | 无界面本地媒体处理 |
| unlimitedStorage | 大文件暂存及本地缓存 |
| sidePanel | 浏览器侧栏界面 |
| declarativeNetRequestWithHostAccess | 特定适配场景的请求规则 |
| http/https 全站访问 | 跨站发现与下载；MAIN/隔离世界内容脚本可能在所有匹配框架运行，存在广泛访问的安全权衡 |

权限并非安全认证。只从可信官方发行入口安装；可在 Chrome 扩展详情中管理站点权限，但限制后部分发现或下载功能可能失效。
