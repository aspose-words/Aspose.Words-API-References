---
title: Paragraph.IsEndOfCell
linktitle: IsEndOfCell
articleTitle: IsEndOfCell
second_title: Aspose.Words for .NET
description: 探索段落的 IsEndOfCell 属性。学习如何识别某个段落是否是单元格中的最后一个段落，从而增强文档结构。
type: docs
weight: 50
url: /zh/net/aspose.words/paragraph/isendofcell/
---
## Paragraph.IsEndOfCell property

如果此段是[`Cell`](../../../aspose.words.tables/cell/) ；否则为假。

```csharp
public bool IsEndOfCell { get; }
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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
