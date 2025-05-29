---
title: Cell.ParentRow
linktitle: ParentRow
articleTitle: ParentRow
second_title: Aspose.Words for .NET
description: 发现 Cell ParentRow 属性可以轻松访问任何单元格的父行，从而增强数据管理和导航效率。
type: docs
weight: 100
url: /zh/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

返回单元格的父行。

```csharp
public Row ParentRow { get; }
```

## 例子

展示如何设置表格以保持在同一页面上。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 为表格中的每个段落启用 KeepWithNext，除了
// 最后一行的最后一个将防止表格分裂到多个页面上。
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true))
    foreach (Paragraph para in cell.Paragraphs)
    {
        Assert.True(para.IsInCell);

        if (!(cell.ParentRow.IsLastRow && para.IsEndOfCell))
            para.ParagraphFormat.KeepWithNext = true;
    }

doc.Save(ArtifactsDir + "Table.KeepTableTogether.docx");
```

### 也可以看看

* class [Row](../../row/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
