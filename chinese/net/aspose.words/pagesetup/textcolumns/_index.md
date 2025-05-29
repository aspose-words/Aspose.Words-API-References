---
title: PageSetup.TextColumns
linktitle: TextColumns
articleTitle: TextColumns
second_title: Aspose.Words for .NET
description: 发现 PageSetup TextColumns 属性，访问多功能的文本列集合，轻松增强文档布局和格式。
type: docs
weight: 420
url: /zh/net/aspose.words/pagesetup/textcolumns/
---
## PageSetup.TextColumns property

返回表示文本列集的集合。

```csharp
public TextColumnCollection TextColumns { get; }
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

* class [TextColumnCollection](../../textcolumncollection/)
* class [PageSetup](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
