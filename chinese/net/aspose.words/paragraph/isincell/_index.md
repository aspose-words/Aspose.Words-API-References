---
title: Paragraph.IsInCell
linktitle: IsInCell
articleTitle: IsInCell
second_title: 用于 .NET 的 Aspose.Words
description: Paragraph IsInCell 财产. 如果此段落是Cell否则为假 在 C#.
type: docs
weight: 100
url: /zh/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

如果此段落是[`Cell`](../../../aspose.words.tables/cell/);否则为假。

```csharp
public bool IsInCell { get; }
```

## 例子

显示如何设置表格以保持在同一页面上。

```csharp
Document doc = new Document(MyDir + "Table spanning two pages.docx");
Table table = doc.FirstSection.Body.Tables[0];

// 为表格中的每个段落启用 KeepWithNext，除了
// 最后一行中的最后一个将防止表拆分为多个页面。
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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
