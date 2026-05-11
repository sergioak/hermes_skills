---
name: hr-overseas-labor-policy
description: "海外劳动政策监控：每周收集越南、墨西哥、波兰、秘鲁、智利五国的劳动法规变化、合规风险预测及典型案例，发邮件给HR。"
version: 1.0.0
author: hermes-user
metadata:
  hermes:
    tags: [hr, labor, overseas, policy, risk, compliance, vietnam, mexico, poland, peru, chile]
---

# HR海外劳动政策监控

每周一早上推送，收集目标国家的劳动政策变动，帮助企业提前规避合规风险。

## 监控国家

越南、墨西哥、波兰、秘鲁、智利

## 内容权重

| 类别 | 权重 | 说明 |
|------|------|------|
| 🟠 政策变化 | 40% | 劳动法规更新、生效时间、对企业影响 |
| 🔴 风险预测 | 40% | 基于政策变化预判潜在违规风险 + 企业应对建议 |
| 🟡 典型案例 | 20% | 该国历史典型违法违规案例、中企教训 |

## 信息源

| 国家 | 主要信息源 |
|------|-----------|
| 越南 | 越南劳动与社会荣军部（molisa.gov.vn）、VNExpress |
| 墨西哥 | STPS官网（.gob.mx）、El Economista |
| 波兰 | 波兰政府官网（gov.pl）、Business Insider Polska |
| 秘鲁 | MINTRA官网（.gob.pe）、Gestión |
| 智利 | DT官网（dt.gob.cl）、La Tercera |

补充：中资商会、ILO、当地法律数据库

## 报告结构

每国家一个板块，每板块 4-6 条内容，严格按权重分配：
- 政策变化 2-3 条
- 风险预测 1-2 条
- 典型案例 0-1 条

## 发送方式

- 报告格式：HTML 邮件
- 收件人：zhangkunjian@boe.com.cn（固定）
- 发送时间：每周一 07:30（如遇节假日顺延）
- 邮件标题：`HR海外劳动政策简报 · YYYY年MM月DD日`

## 文件结构

```
hr-overseas-labor-policy/
  SKILL.md
  references/
    prompt-template.md       # cron job 执行prompt
    email-template.html     # HTML邮件模板
  scripts/
    (共用 ai-daily-newsletter/scripts/send_email.py)
```

## 内容语言规则

- **正文：全部中文**
- **政策名称/条款：附原文**（当地语言 + 英文译名）
- **案例标题：附原文**（当地语言）
- **原文链接**：保留官方链接

## 注意事项

- 政策内容须注明**生效时间**，判断是否已生效或待生效
- 风险预测要具体，不要泛泛而谈，要指出"哪类企业/哪种操作"有风险
- 典型案例优先选中资企业或亚洲企业被查案例
