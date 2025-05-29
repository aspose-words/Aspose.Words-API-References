---
title: Row.PreviousRow
linktitle: PreviousRow
articleTitle: PreviousRow
second_title: Aspose.Words for .NET
description: 访问 PreviousRow 属性可轻松检索前一个 Row 节点，从而增强数据导航并简化编码工作流程。
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

该方法可用于需要对表格行进行类型访问的情况。如果 a [`StructuredDocumentTag`](../../../aspose.words.markup/structureddocumenttag/)节点位于表而不是行中， 它会自动遍历以获取其中包含的行。

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

* class [Row](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
