---
title: Row.NextRow
linktitle: NextRow
articleTitle: NextRow
second_title: Aspose.Words for .NET
description: 发现 NextRow 属性可以轻松访问以下 Row 节点，增强您的数据导航和管理体验。
type: docs
weight: 70
url: /zh/net/aspose.words.tables/row/nextrow/
---
## Row.NextRow property

获取下一个[`Row`](../)节点.

```csharp
public Row NextRow { get; }
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
