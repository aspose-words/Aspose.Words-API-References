---
title: ParagraphFormat.TabStops
linktitle: TabStops
articleTitle: TabStops
second_title: 用于 .NET 的 Aspose.Words
description: ParagraphFormat TabStops 财产. 获取为此对象定义的自定义制表位的集合 在 C#.
type: docs
weight: 390
url: /zh/net/aspose.words/paragraphformat/tabstops/
---
## ParagraphFormat.TabStops property

获取为此对象定义的自定义制表位的集合。

```csharp
public TabStopCollection TabStops { get; }
```

## 例子

显示如何修改 TOC 相关段落中右制表位的位置。

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// 使用基于 TOC 结果的样式遍历所有段落；这是 TOC 和 TOC9 之间的任何样式。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true).OfType<Paragraph>())
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // 获取本段使用的第一个选项卡，这应该是用于对齐页码的选项卡。
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // 替换第一个默认制表符，用自定义制表位停止。
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### 也可以看看

* class [TabStopCollection](../../tabstopcollection/)
* class [ParagraphFormat](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
