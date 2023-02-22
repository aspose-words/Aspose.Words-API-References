---
title: TableStyle.ColumnStripe
second_title: Aspose.Words for .NET API 参考
description: TableStyle 财产. 获取或设置当样式指定奇数/偶数列带时要包含在带中的列数
type: docs
weight: 70
url: /zh/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

获取或设置当样式指定奇数/偶数列带时要包含在带中的列数。

```csharp
public int ColumnStripe { get; set; }
```

### 例子

演示如何创建在行之间交替的条件表样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以配置表格的条件样式，为行/列应用不同的颜色，
// 根据行/列是偶数还是奇数，创建交替的颜色模式。
// 我们也可以将数字 n 应用到行/列绑定，
// 这意味着颜色在每 n 行/列之后交替，而不是一个。
// 创建一个表，其中单个列和行将绑定列将三个绑定。
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

// 设置两种颜色，每 3 行交替显示一次。
tableStyle.RowStripe = 3;
tableStyle.ConditionalStyles[ConditionalStyleType.OddRowBanding].Shading.BackgroundPatternColor = Color.LightBlue;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenRowBanding].Shading.BackgroundPatternColor = Color.LightCyan;

// 设置颜色以应用于每个偶数列，这将覆盖任何自定义行着色。
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// “StyleOptions”属性默认启用行带区。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// 使用“StyleOptions”属性也可以启用列带。
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### 也可以看看

* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../tablestyle/)
* 部件 [Aspose.Words](../../../)


