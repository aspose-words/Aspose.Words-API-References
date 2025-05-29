---
title: TextWrapping Enum
linktitle: TextWrapping
articleTitle: TextWrapping
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Tables.TextWrapping 枚举，实现高效的表格文本环绕。轻松增强您的文档格式！
type: docs
weight: 7230
url: /zh/net/aspose.words.tables/textwrapping/
---
## TextWrapping enumeration

指定文本如何环绕表格。

```csharp
public enum TextWrapping
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 文本和表格按其在文档中出现的顺序显示。 |
| Around | `1` | 文本环绕表格，占据了可用的侧面空间。 |
| Default | `0` | 默认值. |

## 例子

展示如何使用表格文本换行。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

builder.Font.Size = 16;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// 将“TextWrapping”属性设置为“TextWrapping.Around”以使表格在其周围环绕文本，
//并通过设置位置将其推入下面的段落中。
table.TextWrapping = TextWrapping.Around;
table.AbsoluteHorizontalDistance = 100;
table.AbsoluteVerticalDistance = 20;

doc.Save(ArtifactsDir + "Table.WrapText.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
