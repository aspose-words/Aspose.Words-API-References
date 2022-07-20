---
title: ClearFormatting
second_title: Aspose.Words for .NET API 参考
description: 清除此条件样式的格式
type: docs
weight: 100
url: /zh/net/aspose.words/conditionalstyle/clearformatting/
---
## ConditionalStyle.ClearFormatting method

清除此条件样式的格式。

```csharp
public void ClearFormatting()
```

### 例子

显示如何重置条件表样式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("First row");
builder.EndRow();
builder.InsertCell();
builder.Write("Last row");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
table.Style = tableStyle;

// 设置表格样式，将表格第一行的边框涂成红色。
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// 设置表格样式，将表格最后一行的边框涂成蓝色。
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// 下面是使用“ClearFormatting”方法清除条件样式的两种方式。
// 1 - 清除表格特定部分的条件样式：
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - 清除整个表格的条件样式：
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### 也可以看看

* class [ConditionalStyle](../../conditionalstyle)
* 命名空间 [Aspose.Words](../../conditionalstyle)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->