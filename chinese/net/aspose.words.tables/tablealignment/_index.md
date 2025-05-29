---
title: TableAlignment Enum
linktitle: TableAlignment
articleTitle: TableAlignment
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Tables.TableAlignment 枚举，实现最佳的内联表格对齐。轻松精准地增强您的文档格式。
type: docs
weight: 7200
url: /zh/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

指定内联表的对齐方式。

```csharp
public enum TableAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Left | `0` | 表格左对齐。 |
| Center | `1` | 表格居中。 |
| Right | `2` | 表格右对齐。 |

## 例子

展示如何将外框应用于表格。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 将表格与页面中心对齐。
table.Alignment = TableAlignment.Center;

// 清除表格中所有现有的边框和阴影。
table.ClearBorders();
table.ClearShading();

// 为表格轮廓添加绿色边框。
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// 用浅绿色纯色填充单元格。
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Tables](../../aspose.words.tables/)
* 部件 [Aspose.Words](../../)
