---
title: "Aspose::Words::MailMerging::MailMergeCleanupOptions enum"
linktitle: "MailMergeCleanupOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::MailMerging::MailMergeCleanupOptions 枚举。指定在 C++ 中邮件合并期间决定删除哪些项目的选项。"
type: docs
weight: 11000
url: /zh/cpp/aspose.words.mailmerging/mailmergecleanupoptions/
---
## MailMergeCleanupOptions enum


指定在邮件合并期间决定删除哪些项目的选项。

```cpp
enum class MailMergeCleanupOptions
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | 0 | 指定默认值。 |
| RemoveEmptyParagraphs | 1 | 指定是否应从文档中删除包含无数据邮件合并字段的段落。设置此选项后，包含区域开始和结束合并字段且本身为空的段落也会被删除。 |
| RemoveUnusedRegions | 2 | 指定是否应从文档中删除未使用的邮件合并区域。 |
| RemoveUnusedFields | 4 | 指定是否应从文档中删除未使用的合并字段。 |
| RemoveContainingFields | 8 | 指定如果嵌套的合并字段已被删除，是否应从文档中删除包含合并字段的字段（例如 IF）。 |
| RemoveStaticFields | 16 | 指定是否应从文档中删除静态字段。静态字段是指其结果在任何文档更改后保持不变的字段。[Fields](../../aspose.words.fields/)，其结果不存储在文档中且实时计算（如 [FieldListNum](../../aspose.words.fields/fieldtype/)、[FieldSymbol](../../aspose.words.fields/fieldtype/) 等）不被视为静态字段。 |
| RemoveEmptyTableRows | 32 | 指定是否应从文档中删除包含邮件合并区域的空行。 |
| RemoveEmptyTables | 64 | 指定是否从文档中删除包含已使用 [RemoveUnusedRegions](./) 或 [RemoveEmptyTableRows](./) 选项移除的邮件合并区域的表格。 |

## 另见

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
