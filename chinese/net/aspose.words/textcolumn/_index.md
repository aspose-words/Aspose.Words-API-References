---
title: Class TextColumn
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.TextColumn 班级. 表示单个文本列 文本列是成员TextColumnCollection集合.  文本列集合包括文档部分中的所有列
type: docs
weight: 6090
url: /zh/net/aspose.words/textcolumn/
---
## TextColumn class

表示单个文本列。 **文本列**是成员[`TextColumnCollection`](../textcolumncollection/)集合.  **文本列**集合包括文档部分中的所有列。

```csharp
public class TextColumn
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | 获取或设置此列与下一列之间的间距（以磅为单位）。最后一列不需要。 |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | 获取或设置文本列的宽度，以磅为单位。 |

### 评论

**文本列**对象仅用于指定具有自定义宽度和间距的列。如果您希望 文档中的列等宽，请设置 TextColumns。[`EvenlySpaced`](../textcolumncollection/evenlyspaced/)至 **真的**.

当一个新的 **文本列**创建它的宽度和间距设置为零。

### 例子

显示如何创建不均匀间隔的列。

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

// 将第一列设置为窄。
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// 将第二列设置为占用页面边缘内剩余的可用空间。
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


