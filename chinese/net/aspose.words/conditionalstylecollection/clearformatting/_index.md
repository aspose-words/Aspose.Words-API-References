---
title: ConditionalStyleCollection.ClearFormatting
linktitle: ClearFormatting
articleTitle: ClearFormatting
second_title: Aspose.Words for .NET
description: 了解 ConditionalStyleCollection ClearFormatting 方法如何有效地从表中删除所有条件样式，从而增强清晰度和设计感。
type: docs
weight: 150
url: /zh/net/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection.ClearFormatting method

清除表格样式的所有条件样式。

```csharp
public void ClearFormatting()
```

## 例子

展示如何重置条件表样式。

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

// 设置表格样式，将表格第一行的边框颜色设为红色。
tableStyle.ConditionalStyles.FirstRow.Borders.Color = Color.Red;

// 设置表格样式，将表格最后一行的边框颜色设为蓝色。
tableStyle.ConditionalStyles.LastRow.Borders.Color = Color.Blue;

// 以下是两种使用“ClearFormatting”方法清除条件样式的方法。
// 1 - 清除表格特定部分的条件样式：
tableStyle.ConditionalStyles[0].ClearFormatting();

Assert.AreEqual(Color.Empty, tableStyle.ConditionalStyles.FirstRow.Borders.Color);

// 2 - 清除整个表格的条件样式：
tableStyle.ConditionalStyles.ClearFormatting();

Assert.True(tableStyle.ConditionalStyles.All(s => s.Borders.Color == Color.Empty));
```

### 也可以看看

* class [ConditionalStyleCollection](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
