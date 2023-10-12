---
title: Paragraph.IsInCell
second_title: Aspose.Words for .NET API 参考
description: Paragraph 财产. 如果该段落是以下段落的直接子段落则为真Cell否则为假
type: docs
weight: 100
url: /zh/net/aspose.words/paragraph/isincell/
---
## Paragraph.IsInCell property

如果该段落是以下段落的直接子段落，则为真[`Cell`](../../../aspose.words.tables/cell/);否则为假。

```csharp
public bool IsInCell { get; }
```

### 例子

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

* class [Paragraph](../)
* 命名空间 [Aspose.Words](../../paragraph/)
* 部件 [Aspose.Words](../../../)


