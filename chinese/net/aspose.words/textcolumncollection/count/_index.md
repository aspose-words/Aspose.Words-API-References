---
title: TextColumnCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 发现 TextColumnCollection Count 属性可以轻松访问文档部分中的列数，从而增强布局控制。
type: docs
weight: 10
url: /zh/net/aspose.words/textcolumncollection/count/
---
## TextColumnCollection.Count property

获取文档部分的列数。

```csharp
public int Count { get; }
```

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
