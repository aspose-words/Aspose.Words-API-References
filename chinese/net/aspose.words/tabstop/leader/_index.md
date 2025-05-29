---
title: TabStop.Leader
linktitle: Leader
articleTitle: Leader
second_title: Aspose.Words for .NET
description: 探索 TabStop Leader 属性，自定义标签的引线类型，提升文档清晰度和美观度。立即优化您的格式！
type: docs
weight: 40
url: /zh/net/aspose.words/tabstop/leader/
---
## TabStop.Leader property

获取或设置制表符下显示的引出线的类型。

```csharp
public TabLeader Leader { get; set; }
```

## 例子

展示如何修改目录相关段落中右制表位的位置。

```csharp
Document doc = new Document(MyDir + "Table of contents.docx");

// 遍历具有基于 TOC 结果的样式的所有段落；这是 TOC 和 TOC9 之间的任何样式。
foreach (Paragraph para in doc.GetChildNodes(NodeType.Paragraph, true))
    if (para.ParagraphFormat.Style.StyleIdentifier >= StyleIdentifier.Toc1 &&
        para.ParagraphFormat.Style.StyleIdentifier <= StyleIdentifier.Toc9)
    {
        // 获取此段落中使用的第一个制表符，这应该是用于对齐页码的制表符。
        TabStop tab = para.ParagraphFormat.TabStops[0];

        // 用自定义制表位替换第一个默认制表位。
        para.ParagraphFormat.TabStops.RemoveByPosition(tab.Position);
        para.ParagraphFormat.TabStops.Add(tab.Position - 50, tab.Alignment, tab.Leader);
    }

doc.Save(ArtifactsDir + "Styles.ChangeTocsTabStops.docx");
```

### 也可以看看

* enum [TabLeader](../../tableader/)
* class [TabStop](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
