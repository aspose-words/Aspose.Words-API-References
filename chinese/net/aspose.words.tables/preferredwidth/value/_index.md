---
title: PreferredWidth.Value
linktitle: Value
articleTitle: Value
second_title: 用于 .NET 的 Aspose.Words
description: PreferredWidth Value 财产. 获取首选宽度值测量单位在中指定Type属性 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

获取首选宽度值。测量单位在中指定[`Type`](../type/)属性.

```csharp
public double Value { get; }
```

## 例子

演示如何验证表格单元格的首选宽度类型和值。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### 也可以看看

* class [PreferredWidth](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
