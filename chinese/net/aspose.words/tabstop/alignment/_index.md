---
title: TabStop.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words for .NET
description: 发现 TabStop Alignment 属性，轻松自定义制表位处的文本对齐方式，增强文档的布局和可读性。
type: docs
weight: 20
url: /zh/net/aspose.words/tabstop/alignment/
---
## TabStop.Alignment property

获取或设置此制表位处的文本对齐方式。

```csharp
public TabAlignment Alignment { get; set; }
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

* enum [TabAlignment](../../tabalignment/)
* class [TabStop](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
