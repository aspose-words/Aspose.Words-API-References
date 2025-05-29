---
title: ParagraphFormat.KeepWithNext
linktitle: KeepWithNext
articleTitle: KeepWithNext
second_title: Aspose.Words for .NET
description: 了解 ParagraphFormat KeepWithNext 属性如何确保您的段落保持在一起，从而增强文档流程和可读性，获得更精致的外观。
type: docs
weight: 170
url: /zh/net/aspose.words/paragraphformat/keepwithnext/
---
## ParagraphFormat.KeepWithNext property

如果该段落与其后面的段落保持在同一页面上，则为真。

```csharp
public bool KeepWithNext { get; set; }
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

* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
