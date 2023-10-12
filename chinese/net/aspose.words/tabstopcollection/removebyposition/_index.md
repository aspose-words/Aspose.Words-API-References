---
title: TabStopCollection.RemoveByPosition
second_title: Aspose.Words for .NET API 参考
description: TabStopCollection 方法. 从集合中删除指定位置处的制表位
type: docs
weight: 120
url: /zh/net/aspose.words/tabstopcollection/removebyposition/
---
## TabStopCollection.RemoveByPosition method

从集合中删除指定位置处的制表位。

```csharp
public void RemoveByPosition(double position)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | Double | 要删除的制表位的位置（以磅为单位）。 |

### 例子

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

* class [TabStopCollection](../)
* 命名空间 [Aspose.Words](../../tabstopcollection/)
* 部件 [Aspose.Words](../../../)


