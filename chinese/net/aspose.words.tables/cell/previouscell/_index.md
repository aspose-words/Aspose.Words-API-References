---
title: Cell.PreviousCell
linktitle: PreviousCell
articleTitle: PreviousCell
second_title: Aspose.Words for .NET
description: 使用 Cell PreviousCell 属性轻松访问上一个 Cell 节点。增强数据导航并简化编码流程。
type: docs
weight: 110
url: /zh/net/aspose.words.tables/cell/previouscell/
---
## Cell.PreviousCell property

获取上一个[`Cell`](../)节点.

```csharp
public Cell PreviousCell { get; }
```

## 评论

当您需要对单元格进行类型访问时，可以使用该方法[`Row`](../../row/) 如果 a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)节点位于一行而不是一个单元格中，则会自动遍历以获取其中包含的单元格。

## 例子

展示如何枚举所有表格单元格。

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 枚举表格的所有单元格。
for (Row row = table.FirstRow; row != null; row = row.NextRow)
{
    for (Cell cell = row.FirstCell; cell != null; cell = cell.NextCell)
    {
        Console.WriteLine(cell.GetText());
    }
}
```

### 也可以看看

* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
