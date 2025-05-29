---
title: TableStyle.ColumnStripe
linktitle: ColumnStripe
articleTitle: ColumnStripe
second_title: Aspose.Words for .NET
description: 探索 TableStyle ColumnStripe 属性，轻松自定义奇数/偶数列条纹，使您的表格呈现精致、专业的外观。
type: docs
weight: 70
url: /zh/net/aspose.words/tablestyle/columnstripe/
---
## TableStyle.ColumnStripe property

当样式指定奇数/偶数列分段时，获取或设置分段中包含的列数。

```csharp
public int ColumnStripe { get; set; }
```

## 例子

展示如何创建在行之间交替的条件表样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 我们可以配置表格的条件样式，以便对行/列应用不同的颜色，
// 根据行/列是偶数还是奇数，创建交替的颜色模式。
// 我们还可以将数字 n 应用于行/列分段，
// 这意味着颜色每 n 行/列交替一次，而不是一次。
// 创建一个表格，其中单列和单行将以三列为单位排列。
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

// 设置一种颜色应用于每个偶数列，这将覆盖任何自定义行颜色。
tableStyle.ColumnStripe = 1;
tableStyle.ConditionalStyles[ConditionalStyleType.EvenColumnBanding].Shading.BackgroundPatternColor = Color.LightSalmon;

table.Style = tableStyle;

// “StyleOptions”属性默认启用行带。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands,
    table.StyleOptions);

// 使用“StyleOptions”属性也可以启用列带。
table.StyleOptions = table.StyleOptions | TableStyleOptions.ColumnBands;

doc.Save(ArtifactsDir + "Table.AlternatingRowStyles.docx");
```

### 也可以看看

* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
