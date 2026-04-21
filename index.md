# 贴贴 tietie · 隐私政策

**生效日期:2026-04-21**
**最后更新:2026-04-21**

贴贴(以下简称"我们")是一款 AI 表情包生成工具。本隐私政策说明我们如何收集、使用、存储和保护你的信息。请在使用贴贴前仔细阅读。

---

## 一、我们收集哪些信息

### 1. 你主动提供的信息

| 信息 | 收集时机 | 存储位置 |
|---|---|---|
| **Apple ID 标识**(匿名 user_id) | 使用"通过 Apple 登录"时 | Supabase(新加坡) |
| **电子邮件**(可选,Apple private relay) | 登录时由 Apple 转发 | 不存储,仅登录用 |
| **参考图片** | 生成表情包时你上传的照片 | Supabase Storage(临时,生成完成后立即删除) |
| **表情文字标签** | 你在创作页面输入的情绪关键词 | Supabase 数据库(随任务记录保留) |

### 2. 自动收集的信息

| 信息 | 用途 | 存储位置 |
|---|---|---|
| **推送 Token(APNs)** | 用来给你发"生成完成"通知 | Supabase |
| **交易 ID**(Apple IAP) | 充值积分验证、防止重复扣费 | Supabase(永久) |
| **生成任务元数据**(场景名、时间戳、状态) | 展示你的创作历史 | Supabase(永久) |

### 3. 我们**不**收集的信息

- ❌ 精确地理位置
- ❌ 通讯录 / 短信 / 通话记录
- ❌ 设备广告标识符(IDFA)
- ❌ 浏览历史 / 其他 App 使用数据
- ❌ 健康 / 运动 / 生物识别数据

---

## 二、AI 生成的特殊说明

贴贴的核心功能是基于你的参考图生成表情包矩阵。这个过程涉及第三方 AI 服务:

- **你的参考图**会短暂发送给 AI 服务商("灵芽 AI",域名 `api.lingyaai.cn`)用于生成
- **AI 返回的生成结果**会存储在 AI 服务商的 CDN(`webstatic.aiproxy.vip`),**2 小时后自动过期删除**
- 贴贴**不会**把你的参考图或生成结果用于训练 AI 模型
- 你上传的参考图在生成完成后,**立即从我们的服务器删除**(由客户端主动触发清理)

---

## 三、我们如何使用这些信息

- 生成你请求的 AI 表情包矩阵
- 给你发送"生成完成"推送通知
- 验证你的 Apple IAP 充值并发放积分
- 展示你的创作历史
- 诊断 bug、提升稳定性

**我们不会**将你的信息用于广告、不会卖给第三方、不会做用户画像分析。

---

## 四、信息共享

我们只在以下场景把信息分享给第三方,且仅限必要范围:

| 第三方 | 分享什么 | 为什么 |
|---|---|---|
| **Apple Inc.** | Apple ID 标识、IAP 交易 ID | Sign in with Apple 登录、IAP 充值验证 |
| **Supabase(新加坡)** | 账号、交易、任务记录 | 我们的后端数据库和推送服务 |
| **灵芽 AI**(`api.lingyaai.cn`) | 你上传的参考图 + 生成提示词 | AI 生成表情包(处理完即删) |

以上三方均遵守各自的隐私政策。我们不与任何其他方共享你的个人信息。

---

## 五、数据存储和保留

- **存储位置**:Supabase 服务器位于**新加坡**(ap-southeast-1 区域)
- **参考图**:生成完成后**立即删除**,不保留
- **AI 生成结果**:灵芽 CDN **2 小时后自动过期**,我们不长期保存
- **账号信息 / 交易记录 / 创作历史**:在你使用贴贴期间持续保留
- **注销账号后**:我们会在 30 天内删除所有与你相关的个人数据(法律要求保留的财务/交易记录除外)

---

## 六、你的权利

在贴贴 App 内,你可以:

- **查看**你的创作历史和积分记录
- **删除**单条生成结果
- **注销账号**并删除所有数据(通过"我的"→"设置"→"注销账号")

如需其他请求(如完整数据导出、更正错误信息),请发邮件至下方联系方式。

---

## 七、儿童隐私

贴贴**不面向 13 岁以下儿童**。我们不会故意收集 13 岁以下儿童的个人信息。如果你是家长或监护人,发现孩子未经同意使用了贴贴,请联系我们删除其信息。

---

## 八、安全措施

- 所有数据传输使用 HTTPS / TLS 加密
- Supabase 数据库启用 Row Level Security(RLS),用户只能访问自己的数据
- IAP 交易通过 Apple 官方 App Store Server API 二次验证,防止伪造

---

## 九、政策变更

我们可能会更新本隐私政策。重大变更时,会通过 App 内通知或推送告知你。继续使用贴贴即视为你接受更新后的政策。

---

## 十、联系我们

隐私相关问题请联系:

- **邮箱**:luo.g.robben@gmail.com
- **开发者**:罗娟(Juan Luo)
- **Apple Developer Team ID**:2W953U82P9

---

## Privacy Policy (English Summary)

**Effective Date: 2026-04-21**

Tietie (贴贴) is an AI sticker generation tool. We collect:
- Apple ID identifier (for Sign in with Apple)
- APNs push token (for notifications)
- Reference images you upload (temporarily, deleted after generation)
- AI-generated stickers (stored on third-party AI CDN for 2 hours, auto-expires)
- IAP transaction records (for credit verification)

We do NOT collect: location, contacts, IDFA, browsing history, health data.

Your reference images are sent to our AI partner (`api.lingyaai.cn`) for generation only, NOT used to train AI models. They are deleted from our servers immediately after generation.

Data is stored on Supabase (Singapore region). You can delete your account from within the app; we erase all personal data within 30 days (except legally required financial records).

For privacy inquiries: luo.g.robben@gmail.com

This app is not intended for children under 13.

---

*本隐私政策的最新版本始终以本页面为准。如有中英文冲突,以中文版为准。*
