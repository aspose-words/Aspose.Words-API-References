---
title: TableStyle.RowStripe
linktitle: RowStripe
articleTitle: RowStripe
second_title: 用于 .NET 的 Aspose.Words
description: TableStyle RowStripe 财产. 获取或设置当样式指定奇数/偶数行分段时要包含在分段中的行数 在 C#.
type: docs
weight: 120
url: /zh/net/aspose.words/tablestyle/rowstripe/
---
## TableStyle.RowStripe property

获取或设置当样式指定奇数/偶数行分段时要包含在分段中的行数。

```csharp
public int RowStripe { get; set; }
```

## 例子

演示如何创建在行之间交替的条件表样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以配置表格的条件样式以将不同的颜色应用于行/列，
// 根据行/列是偶数还是奇数，创建交替颜色模式。
// 我们还可以将数字 n 应用于行/列带，
// 意味着颜色在每 n 行/列而不是每 n 行/列之后交替。
// 创建一个表，其中单列和行将排列，列将排列为三个。
Table table = builder.StartTable();
for (int i = 0; i < 15; i++)
{
    for (int j = 0; j < 4; j++)
    {
        builder.InsertCell();
        builder.Writeln($"{(j % 2 == 0 ? "Even" : "Odd")} column.");
        builder.Write($"Row banding {(i % 3 == 0 ? "start" : "continuation")}.");
    }
    builder.EndRow();
}
builder.EndTable();

// 将线条样式应用于表格的所有边框。
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Borders.Color = Color.Black;
tableStyle.Borders.LineStyle = LineStyle.Double;

// 设置两种颜色，每 3 行交替一次。
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// 设置应用于每个偶数列的颜色，这将覆盖任何自定义行着色。
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// “StyleOptions”属性默认启用行分隔。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// 还可以使用“StyleOptions”属性来启用列带。
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### 也可以看看

* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
