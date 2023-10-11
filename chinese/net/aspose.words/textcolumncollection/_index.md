---
title: Class TextColumnCollection
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.TextColumnCollection 班级. 的集合TextColumn表示文档某个部分中所有文本列的对象
type: docs
weight: 6400
url: /zh/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

的集合[`TextColumn`](../textcolumn/)表示文档某个部分中所有文本列的对象。

要了解更多信息，请访问[使用部分](https://docs.aspose.com/words/net/working-with-sections/)文档文章。

```csharp
public class TextColumnCollection
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | 获取文档部分中的列数。 |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | 如果文本列宽度相等且间隔均匀，则为 True。 |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | 返回指定索引处的文本列。 |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | 当`真的`，在列之间添加一条垂直线。 |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | 当列均匀分布时，获取或设置每列之间的间距（以点为单位）。 |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | 当列均匀分布时，获取列的宽度。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | 将文本排列到指定数量的文本列中。 |

### 评论

使用[`SetCount`](./setcount/)设置文本列的数量。

要使所有列的宽度相等且间隔均匀，请设置[`EvenlySpaced`](./evenlyspaced/)到`真的` 并指定列之间的空间量[`Spacing`](./spacing/)。 MS Word 将 自动计算列宽。

如果你有[`EvenlySpaced`](./evenlyspaced/)设置`错误的`，您需要单独指定每个 列的宽度和间距。使用索引器访问个人[`TextColumn`](../textcolumn/)对象。

使用自定义列宽时，请确保所有列宽和它们之间的间距 的总和等于页面宽度减去左右页边距。

### 例子

演示如何在一个部分中创建多个均匀间隔的列。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)


