---
title: TextColumnCollection.Width
linktitle: Width
articleTitle: Width
second_title: Aspose.Words for .NET
description: 探索 TextColumnCollection 的 Width 属性。轻松管理均匀分布的列，实现项目的最佳布局和设计。
type: docs
weight: 60
url: /zh/net/aspose.words/textcolumncollection/width/
---
## TextColumnCollection.Width property

当列间距均匀时，获取列的宽度。

```csharp
public double Width { get; }
```

## 评论

仅在以下情况下有效[`EvenlySpaced`](../evenlyspaced/)设置为`真的`。

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
