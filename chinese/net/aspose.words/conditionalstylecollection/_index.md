---
title: ConditionalStyleCollection Class
linktitle: ConditionalStyleCollection
articleTitle: ConditionalStyleCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.ConditionalStyleCollection 班级. 代表一个集合ConditionalStyle对象 在 C#.
type: docs
weight: 320
url: /zh/net/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class

代表一个集合[`ConditionalStyle`](../conditionalstyle/)对象.

```csharp
public sealed class ConditionalStyleCollection : IEnumerable<ConditionalStyle>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BottomLeftCell](../../aspose.words/conditionalstylecollection/bottomleftcell/) { get; } | 获取左下角单元格样式。 |
| [BottomRightCell](../../aspose.words/conditionalstylecollection/bottomrightcell/) { get; } | 获取右下角单元格样式。 |
| [Count](../../aspose.words/conditionalstylecollection/count/) { get; } | 获取集合中条件样式的数量。 |
| [EvenColumnBanding](../../aspose.words/conditionalstylecollection/evencolumnbanding/) { get; } | 获取偶数列带状样式。 |
| [EvenRowBanding](../../aspose.words/conditionalstylecollection/evenrowbanding/) { get; } | 获取偶数行条带样式。 |
| [FirstColumn](../../aspose.words/conditionalstylecollection/firstcolumn/) { get; } | 获取第一列样式。 |
| [FirstRow](../../aspose.words/conditionalstylecollection/firstrow/) { get; } | 获取第一行样式。 |
| [Item](../../aspose.words/conditionalstylecollection/item/) { get; } | 检索一个[`ConditionalStyle`](../conditionalstyle/)按条件样式类型的对象。 (2 indexers) |
| [LastColumn](../../aspose.words/conditionalstylecollection/lastcolumn/) { get; } | 获取最后一列样式。 |
| [LastRow](../../aspose.words/conditionalstylecollection/lastrow/) { get; } | 获取最后一行样式。 |
| [OddColumnBanding](../../aspose.words/conditionalstylecollection/oddcolumnbanding/) { get; } | 获取奇数列带状样式。 |
| [OddRowBanding](../../aspose.words/conditionalstylecollection/oddrowbanding/) { get; } | 获取奇数行带状样式。 |
| [TopLeftCell](../../aspose.words/conditionalstylecollection/topleftcell/) { get; } | 获取左上角单元格样式。 |
| [TopRightCell](../../aspose.words/conditionalstylecollection/toprightcell/) { get; } | 获取右上角的单元格样式。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [ClearFormatting](../../aspose.words/conditionalstylecollection/clearformatting/)() | 清除表格样式的所有条件样式。 |
| [GetEnumerator](../../aspose.words/conditionalstylecollection/getenumerator/)() | 返回一个可用于迭代集合中所有条件样式的枚举器对象。 |

## 评论

无法在此集合中添加或删除项目。它包含一组永久的项目：一个项目 for 的每个值[`ConditionalStyleType`](../conditionalstyletype/)枚举类型.

## 例子

显示如何使用表格的某些区域样式。

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

// 条件样式是只影响部分表格单元格的格式更改
// 基于谓词，例如最后一行的单元格。
// 下面是从“ConditionalStyles”集合中访问表格样式条件样式的三种方法。
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

// 将包含所有条件样式的自定义样式应用于表格。
table.Style = tableStyle;

// 我们的样式默认应用一些条件样式。
Assert.AreEqual(TableStyleOptions.FirstRow | TableStyleOptions.FirstColumn | TableStyleOptions.RowBands, 
    table.StyleOptions);

// 我们需要通过“StyleOptions”属性自己启用所有其他样式。
table.StyleOptions = table.StyleOptions | TableStyleOptions.LastRow | TableStyleOptions.LastColumn;

doc.Save(ArtifactsDir + "Table.ConditionalStyles.docx");
```

### 也可以看看

* class [ConditionalStyle](../conditionalstyle/)
* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
