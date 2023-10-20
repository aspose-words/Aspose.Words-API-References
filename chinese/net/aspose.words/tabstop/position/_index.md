---
title: TabStop.Position
linktitle: Position
articleTitle: Position
second_title: 用于 .NET 的 Aspose.Words
description: TabStop Position 财产. 获取制表位的位置以磅为单位 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/tabstop/position/
---
## TabStop.Position property

获取制表位的位置（以磅为单位）。

```csharp
public double Position { get; }
```

## 例子

演示如何修改目录相关段落中右侧制表位的位置。

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// 使用基于 TOC 结果的样式迭代所有段落；这是 TOC 和 TOC9 之间的任何样式。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // 获取本段中使用的第一个制表符，这应该是用于对齐页码的制表符。
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // 将第一个默认制表符替换为自定义制表符停止位。
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### 也可以看看

* class [TabStop](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
