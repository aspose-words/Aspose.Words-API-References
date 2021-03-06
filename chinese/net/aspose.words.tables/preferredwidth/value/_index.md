---
title: Value
second_title: Aspose.Words for .NET API 参考
description: 获取首选宽度值计量单位在Typeaspose.words.tables/preferredwidth/type属性.
type: docs
weight: 50
url: /zh/net/aspose.words.tables/preferredwidth/value/
---
## PreferredWidth.Value property

获取首选宽度值。计量单位在[`Type`](../type)属性.

```csharp
public double Value { get; }
```

### 例子

显示如何验证表格单元格的首选宽度类型和值。

```csharp
Document doc = new Document(MyDir + "Tables.docx");

Table table = doc.FirstSection.Body.Tables[0];
Cell firstCell = table.FirstRow.FirstCell;

Assert.AreEqual(PreferredWidthType.Percent, firstCell.CellFormat.PreferredWidth.Type);
Assert.AreEqual(11.16d, firstCell.CellFormat.PreferredWidth.Value);
```

### 也可以看看

* class [PreferredWidth](../../preferredwidth)
* 命名空间 [Aspose.Words.Tables](../../preferredwidth)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
