---
title: SdtAppearance Enum
linktitle: SdtAppearance
articleTitle: SdtAppearance
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Markup.SdtAppearance 枚举，用于自定义结构化文档标签的外观。轻松增强您的文档格式！
type: docs
weight: 4680
url: /zh/net/aspose.words.markup/sdtappearance/
---
## SdtAppearance enumeration

指定结构化文档标签的外观。

```csharp
public enum SdtAppearance
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| BoundingBox | `0` | 表示显示为阴影矩形或边界框的结构化文档标签。 |
| Tags | `1` | 表示以开始和结束标记显示的结构化文档标签。 |
| Hidden | `2` | 表示未显示的结构化文档标签。 |
| Default | `0` | 默认为BoundingBox. |

## 例子

展示如何在内容周围显示标签。

```csharp
Document doc = new Document(MyDir + "Multi-section structured document tags.docx");
StructuredDocumentTagRangeStart tag =
    doc.GetChild(NodeType.StructuredDocumentTagRangeStart, 0, true) as StructuredDocumentTagRangeStart;

if (tag.Appearance == SdtAppearance.Hidden)
    tag.Appearance = SdtAppearance.Tags;
```

### 也可以看看

* 命名空间 [Aspose.Words.Markup](../../aspose.words.markup/)
* 部件 [Aspose.Words](../../)
