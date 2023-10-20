---
title: Cell.Paragraphs
linktitle: Paragraphs
articleTitle: Paragraphs
second_title: 用于 .NET 的 Aspose.Words
description: Cell Paragraphs 财产. 获取作为单元格直接子级的段落的集合 在 C#.
type: docs
weight: 90
url: /zh/net/aspose.words.tables/cell/paragraphs/
---
## Cell.Paragraphs property

获取作为单元格直接子级的段落的集合。

```csharp
public ParagraphCollection Paragraphs { get; }
```

## 例子

展示如何将表格设置为在同一页面上保持在一起。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 对表中的每个段落启用 KeepWithNext，除了
// 最后一行中的最后一个将防止表格拆分为多个页面。
foreach (Cell cell in table.GetChildNodes(NodeType.Cell, true).OfType<Cell>())
    foreach (Paragraph para in cell.Paragraphs.OfType<Paragraph>())
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
