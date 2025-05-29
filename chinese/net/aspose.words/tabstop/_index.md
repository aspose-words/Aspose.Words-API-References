---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TabStop 类，这是您在文档格式化中自定义制表位的解决方案。轻松精准地增强您的文档！
type: docs
weight: 7050
url: /zh/net/aspose.words/tabstop/
---
## TabStop class

代表单个自定义制表位。`TabStop`对象是 的成员[`TabStopCollection`](../tabstopcollection/)收藏.

要了解更多信息，请访问[Aspose.Words 文档对象模型（DOM）](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

```csharp
public sealed class TabStop
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [TabStop](tabstop/#constructor)(*double*) | 初始化此类的新实例。 |
| [TabStop](tabstop/#constructor_1)(*double, [TabAlignment](../tabalignment/), [TabLeader](../tableader/)*) | 初始化此类的新实例。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Alignment](../../aspose.words/tabstop/alignment/) { get; set; } | 获取或设置此制表位处的文本对齐方式。 |
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | 返回`真的`如果此制表位清除了此位置上所有现有的制表位。 |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | 获取或设置制表符下显示的引出线的类型。 |
| [Position](../../aspose.words/tabstop/position/) { get; } | 获取制表位的位置（以点为单位）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | 与指定的`TabStop`. |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | 计算此对象的哈希码。 |

## 评论

通常，制表位会指定制表位所在的位置。但由于制表位可以从父样式继承，因此子对象可能需要明确定义在给定位置没有制表位。要清除给定位置的继承制表位，请创建一个`TabStop`对象和 set [`Alignment`](./alignment/)到Clear。

有关详细信息，请参阅[`TabStopCollection`](../tabstopcollection/)。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
