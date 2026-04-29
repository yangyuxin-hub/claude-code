# 飞书多维表格操作速查

> Base Token: Xg4wbrz8EaUzPlstdhYc0KUjnBg
> 更新时间: 2026-04-01

---

## 选题库（tblJ9VarszpjX78N）

### 字段结构

| 字段名 | 类型 | field_id |
|--------|------|----------|
| 标题 | text | fldfXV03Rp |
| 写作角度 | text | fld50VlKes |
| 备注 | text | fldCR7mzEO |
| 平台 | select | fld33dNWmx |
| 分类 | select | fldfy4ur5a |
| 状态 | select | fldzmIeKxt |

### 状态选项
- 🔥今天必写
- ⚡本周可写
- 📌积累备用
- ✅已发布

### 新增选题

```bash
lark-cli base +record-upsert \
  --base-token "Xg4wbrz8EaUzPlstdhYc0KUjnBg" \
  --table-id "tblJ9VarszpjX78N" \
  --json '{
    "标题": "文章标题",
    "写作角度": "切入角度说明",
    "平台": "公众号",
    "分类": "热点解读",
    "状态": "⚡本周可写",
    "备注": "补充说明"
  }'
```

### 更新状态（已有记录）

```bash
lark-cli base +record-upsert \
  --base-token "Xg4wbrz8EaUzPlstdhYc0KUjnBg" \
  --table-id "tblJ9VarszpjX78N" \
  --record-id "recXXXXXXXX" \
  --json '{"状态": "✅已发布"}'
```

---

## 素材库（tblXXufLC4VxIi7h）

### 字段结构

| 字段名 | 类型 | field_id |
|--------|------|----------|
| 标题 | text | fldpBLqywv |
| 链接 | text(url) | fldCGcWiqc |
| 内容介绍 | text | fld5Zxyutp |
| 来源 | select | fldgosG2MS |
| 分类 | select | fld0ZjeTVp |
| 状态 | select | fldkI6CpJI |
| 适合度 | select | fldsMtu9ad |
| 写作角度 | text | fldl7UTM2z |

### 状态选项
- 📥待消化
- 💡已转选题
- ⏸暂时搁置

### 适合度选项
- ✅ 适合
- ⚠️ 待定
- ❌ 不适合

### 新增素材

```bash
lark-cli base +record-upsert \
  --base-token "Xg4wbrz8EaUzPlstdhYc0KUjnBg" \
  --table-id "tblXXufLC4VxIi7h" \
  --json '{
    "标题": "文章/内容标题",
    "链接": "https://...",
    "来源": "公众号",
    "内容介绍": "主要讲了什么",
    "分类": "热点解读",
    "状态": "📥待消化",
    "适合度": "⚠️ 待定",
    "写作角度": "可能的切入角度"
  }'
```

---

## 常用查询

### 查看所有「本周可写」选题

```bash
lark-cli base +record-list \
  --base-token "Xg4wbrz8EaUzPlstdhYc0KUjnBg" \
  --table-id "tblJ9VarszpjX78N" \
  --limit 50
```

### 统计各状态数量

```bash
lark-cli base +data-query \
  --base-token "Xg4wbrz8EaUzPlstdhYc0KUjnBg" \
  --table-id "tblJ9VarszpjX78N" \
  --json '{
    "group_by": [{"field_name": "状态"}],
    "metrics": [{"type": "COUNT", "field_name": "标题"}]
  }'
```
