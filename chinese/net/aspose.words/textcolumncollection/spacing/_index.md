---
title: TextColumnCollection.Spacing
linktitle: Spacing
articleTitle: Spacing
second_title: Aspose.Words for .NET
description: 探索 TextColumnCollection Spacing 属性，轻松管理以点为单位的列间距，打造精致专业的布局。立即提升您的设计！
type: docs
weight: 50
url: /zh/net/aspose.words/textcolumncollection/spacing/
---
## TextColumnCollection.Spacing property

当列间距均匀时，获取或设置每列之间的间距量（以磅为单位）。

```csharp
public double Spacing { get; set; }
```

## 评论

仅在以下情况下有效[`EvenlySpaced`](../evenlyspaced/)设置为`真的`.

## 例子

展示如何在一个部分中创建多个间距均匀的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### 也可以看看

* class [TextColumnCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
