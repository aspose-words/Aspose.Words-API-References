---
title: ConditionalStyleCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words for .NET
description: 发现 ConditionalStyleCollection Item 属性以便按类型轻松访问 ConditionalStyle 对象，从而毫不费力地增强您的样式功能。
type: docs
weight: 80
url: /zh/net/aspose.words/conditionalstylecollection/item/
---
## ConditionalStyleCollection indexer (1 of 2)

检索[`ConditionalStyle`](../../conditionalstyle/)按条件样式类型对象.

```csharp
public ConditionalStyle this[ConditionalStyleType conditionalStyleType] { get; }
```

## 例子

展示如何使用表格的某些区域样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// 创建自定义表格样式。
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// 条件样式是仅影响部分表格单元格的格式更改
// 基于谓词，例如单元格位于最后一行。
// 以下是从“ConditionalStyles”集合中访问表格样式的条件样式的三种方法。
// 1 - 按样式类型：
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - 按索引：
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - 作为属性：
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// 将填充和文本格式应用于条件样式。
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// 列出所有可能的样式条件。
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// 将包含所有条件样式的自定义样式应用到表格。
table.Style = tableStyle;

// 我们的样式默认应用一些条件样式。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// 我们需要通过“StyleOptions”属性自行启用所有其他样式。
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### 也可以看看

* class [ConditionalStyle](../../conditionalstyle/)
* enum [ConditionalStyleType](../../conditionalstyletype/)
* class [ConditionalStyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## ConditionalStyleCollection indexer (2 of 2)

检索[`ConditionalStyle`](../../conditionalstyle/)按索引排序的对象.

```csharp
public ConditionalStyle this[int index] { get; }
```

| 范围 | 描述 |
| --- | --- |
| index | 要检索的条件样式的从零开始的索引。 |

## 例子

展示如何使用表格的某些区域样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Cell 1");
builder.InsertCell();
builder.Write("Cell 2");
builder.EndRow();
builder.InsertCell();
builder.Write("Cell 3");
builder.InsertCell();
builder.Write("Cell 4");
builder.EndTable();

// 创建自定义表格样式。
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");

// 条件样式是仅影响部分表格单元格的格式更改
// 基于谓词，例如单元格位于最后一行。
// 以下是从“ConditionalStyles”集合中访问表格样式的条件样式的三种方法。
// 1 - 按样式类型：
tableStyle.ConditionalStyles[ConditionalStyleType.FirstRow].Shading.BackgroundPatternColor = Color.AliceBlue;

// 2 - 按索引：
tableStyle.ConditionalStyles[0].Borders.Color = Color.Black;
tableStyle.ConditionalStyles[0].Borders.LineStyle = LineStyle.DotDash;
Assert.AreEqual(ConditionalStyleType.FirstRow, tableStyle.ConditionalStyles[0].Type);

// 3 - 作为属性：
tableStyle.ConditionalStyles.FirstRow.ParagraphFormat.Alignment = ParagraphAlignment.Center;

// 将填充和文本格式应用于条件样式。
tableStyle.ConditionalStyles.LastRow.BottomPadding = 10;
tableStyle.ConditionalStyles.LastRow.LeftPadding = 10;
tableStyle.ConditionalStyles.LastRow.RightPadding = 10;
tableStyle.ConditionalStyles.LastRow.TopPadding = 10;
tableStyle.ConditionalStyles.LastColumn.Font.Bold = true;

// 列出所有可能的样式条件。
using (IEnumerator<ConditionalStyle> enumerator = tableStyle.ConditionalStyles.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        ConditionalStyle currentStyle = enumerator.Current;
        if (currentStyle != null) Console.WriteLine(currentStyle.Type);
    }
}

// 将包含所有条件样式的自定义样式应用到表格。
table.Style = tableStyle;

// 我们的样式默认应用一些条件样式。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// 我们需要通过“StyleOptions”属性自行启用所有其他样式。
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### 也可以看看

* class [ConditionalStyle](../../conditionalstyle/)
* class [ConditionalStyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
