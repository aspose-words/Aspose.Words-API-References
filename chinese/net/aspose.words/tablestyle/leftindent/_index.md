---
title: TableStyle.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words for .NET
description: 探索 TableStyle LeftIndent 属性，轻松自定义表格的左缩进，以增强布局控制和视觉吸引力。
type: docs
weight: 90
url: /zh/net/aspose.words/tablestyle/leftindent/
---
## TableStyle.LeftIndent property

获取或设置代表表格左缩进的值。

```csharp
public double LeftIndent { get; set; }
```

## 例子

展示如何设置表格的位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 以下是两种水平对齐表格的方法。
// 1 - 使用“Alignment”属性将其对齐到页面上的某个位置，例如中心：
TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.Alignment = TableAlignment.Center;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.Single;

// 插入一个表格并将我们创建的样式应用到它。
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned to the center of the page");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

// 2 - 使用“LeftIndent”指定从页面左边距的缩进：
tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle2");
tableStyle.LeftIndent = 55;
tableStyle.Borders.Color = Color.Green;
tableStyle.Borders.LineStyle = LineStyle.Single;

table = builder.StartTable();
builder.InsertCell();
builder.Write("Aligned according to left indent");
builder.EndTable();
table.PreferredWidth = PreferredWidth.FromPoints(300);

table.Style = tableStyle;

doc.Save(ArtifactsDir + "Table.SetTableAlignment.docx");
```

### 也可以看看

* class [TableStyle](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
