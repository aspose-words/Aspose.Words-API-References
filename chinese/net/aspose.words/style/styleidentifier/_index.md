---
title: Style.StyleIdentifier
linktitle: StyleIdentifier
articleTitle: StyleIdentifier
second_title: Aspose.Words for .NET
description: 探索内置样式中与语言环境无关的 StyleIdentifier 属性。使用一致且灵活的样式解决方案来增强您的项目。
type: docs
weight: 180
url: /zh/net/aspose.words/style/styleidentifier/
---
## Style.StyleIdentifier property

获取内置样式的区域独立样式标识符。

```csharp
public StyleIdentifier StyleIdentifier { get; }
```

## 评论

对于用户定义（自定义）样式，此属性返回User。

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

* enum [StyleIdentifier](../../styleidentifier/)
* class [Style](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
