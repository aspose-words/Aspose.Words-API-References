---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TextColumn 类，用于管理文档中的文本列。轻松访问和自定义文本部分的每一列。
type: docs
weight: 7240
url: /zh/net/aspose.words/textcolumn/
---
## TextColumn class

代表单个文本列。`TextColumn`是[`TextColumnCollection`](../textcolumncollection/)collection. 该`TextColumn`集合包括文档某一部分的所有列。

要了解更多信息，请访问[使用部分](https://docs.aspose.com/words/net/working-with-sections/)文档文章。

```csharp
public class TextColumn
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | 获取或设置此列与下一列之间的间距（以磅为单位）。最后一列不需要。 |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | 获取或设置文本列的宽度（以磅为单位）。 |

## 评论

`TextColumn`对象仅用于指定具有自定义宽度和间距的列。如果您希望文档中的列宽度相等，请设置 TextColumns。[`EvenlySpaced`](../textcolumncollection/evenlyspaced/)到`真的`。

当一个新的`TextColumn`创建后其宽度和间距设置为零。

## 例子

展示如何创建间距不均匀的列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// 确定我们可用于排列列的空间量。
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// 将第一列设置为窄列。
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// 设置第二列以占据页面边缘内剩余的可用空间。
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
