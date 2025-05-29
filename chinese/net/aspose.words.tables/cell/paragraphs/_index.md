---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: Aspose.Words for .NET
description: 发现单元格段落属性来访问直接子段落的集合，增强文档的结构和可读性。
type: docs
weight: 90
url: /zh/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

获取单元格的直接子段落的集合。

```csharp
public ParagraphCollection Paragraphs { get; }
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

* class [ParagraphCollection](../../../aspose.words/paragraphcollection/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../../aspose.words.tables/)
* 部件 [Aspose.Words](../../../)
