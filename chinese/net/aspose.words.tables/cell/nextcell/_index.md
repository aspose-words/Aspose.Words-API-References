---
title: Cell.NextCell
linktitle: NextCell
articleTitle: NextCell
second_title: 用于 .NET 的 Aspose.Words
description: Cell NextCell 财产. 获取下一个Cell节点 在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.tables/cell/nextcell/
---
## Cell.NextCell property

获取下一个[`Cell`](../)节点.

```csharp
public Cell NextCell { get; }
```

## 评论

当您需要对单元格进行键入访问时，可以使用该方法[`Row`](../../row/)。如果a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)节点在一行而不是单元格中找到，它会自动 遍历以获取包含在. 内的单元格

## 例子

演示如何枚举所有表格单元格。

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
