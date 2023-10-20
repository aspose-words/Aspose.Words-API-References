---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: 用于 .NET 的 Aspose.Words
description: Row PreviousRow 财产. 获取上一个Row节点 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words.tables/row/previousrow/
---
## Row.PreviousRow property

获取上一个[`Row`](../)节点.

```csharp
public Row PreviousRow { get; }
```

## 评论

当您需要对表行进行类型访问时，可以使用该方法。如果a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)在表中而不是行中找到节点， 会自动遍历它以获取其中包含的行。

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

* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
