---
title: ConditionalStyle Class
linktitle: ConditionalStyle
articleTitle: ConditionalStyle
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ConditionalStyle 类，实现高级表格格式化。使用动态样式增强您的文档，轻松提升可读性。
type: docs
weight: 510
url: /zh/net/aspose.words/conditionalstyle/
---
## ConditionalStyle class

表示对具有指定表格样式的表格的某些区域应用特殊格式。

要了解更多信息，请访问[使用表格](https://docs.aspose.com/words/net/working-with-tables/)文档文章。

```csharp
public sealed class ConditionalStyle
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Borders](../../aspose.words/conditionalstyle/borders/) { get; } | 获取条件样式的默认单元格边框集合。 |
| [BottomPadding](../../aspose.words/conditionalstyle/bottompadding/) { get; set; } | 获取或设置在表格单元格内容下方添加的空间量（以点为单位）。 |
| [Font](../../aspose.words/conditionalstyle/font/) { get; } | 获取条件样式的字符格式。 |
| [LeftPadding](../../aspose.words/conditionalstyle/leftpadding/) { get; set; } | 获取或设置在表格单元格内容左侧添加的空间量（以点为单位）。 |
| [ParagraphFormat](../../aspose.words/conditionalstyle/paragraphformat/) { get; } | 获取条件样式的段落格式。 |
| [RightPadding](../../aspose.words/conditionalstyle/rightpadding/) { get; set; } | 获取或设置在表格单元格内容右侧添加的空间量（以点为单位）。 |
| [Shading](../../aspose.words/conditionalstyle/shading/) { get; } | 获得[`Shading`](../shading/)引用此条件样式的阴影格式的对象。 |
| [TopPadding](../../aspose.words/conditionalstyle/toppadding/) { get; set; } | 获取或设置在表格单元格内容上方添加的空间量（以点为单位）。 |
| [Type](../../aspose.words/conditionalstyle/type/) { get; } | 获取与此条件样式相关的表格区域。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstyle/clearformatting/)() | 清除此条件样式的格式。 |
| override [Equals](../../aspose.words/conditionalstyle/equals/)(*object*) | 将此条件样式与指定对象进行比较。 |
| override [GetHashCode](../../aspose.words/conditionalstyle/gethashcode/)() | 计算此对象的哈希码。 |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
