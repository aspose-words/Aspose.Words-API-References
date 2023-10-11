---
title: Cell.ParentRow
second_title: Aspose.Words for .NET API 参考
description: Cell 财产. 返回单元格的父行
type: docs
weight: 100
url: /zh/net/aspose.words.tables/cell/parentrow/
---
## Cell.ParentRow property

返回单元格的父行。

```csharp
public Row ParentRow { get; }
```

### 评论

相当于FirstNonMarkupParentNode投射到[`Row`](../../row/)。

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

* class [Row](../../row/)
* class [Cell](../)
* 命名空间 [Aspose.Words.Tables](../../cell/)
* 部件 [Aspose.Words](../../../)


