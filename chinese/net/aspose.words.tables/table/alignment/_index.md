---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words for .NET
description: 发现表格对齐属性，轻松控制文档中的内联表格定位，以获得精致、专业的外观。
type: docs
weight: 40
url: /zh/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

指定内联表格在文档中的对齐方式。

```csharp
public TableAlignment Alignment { get; set; }
```

## 评论

默认值为Left。

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

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
