---
title: TabStop Class
linktitle: TabStop
articleTitle: TabStop
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.TabStop 班级. 表示单个自定义制表位这TabStop对象是 the 的成员TabStopCollection集合 在 C#.
type: docs
weight: 6200
url: /zh/net/aspose.words/tabstop/
---
## TabStop class

表示单个自定义制表位。这`TabStop`对象是 the 的成员[`TabStopCollection`](../tabstopcollection/)集合.

要了解更多信息，请访问[Aspose.Words 文档对象模型 (DOM)](https://docs.aspose.com/words/net/aspose-words-document-object-model/)文档文章。

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
| [IsClear](../../aspose.words/tabstop/isclear/) { get; } | 返回`真的`如果此制表位清除此位置的任何现有制表位。 |
| [Leader](../../aspose.words/tabstop/leader/) { get; set; } | 获取或设置制表符下显示的引导线类型。 |
| [Position](../../aspose.words/tabstop/position/) { get; } | 获取制表位的位置（以磅为单位）。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [Equals](../../aspose.words/tabstop/equals/#equals)(*TabStop*) | 与指定的比较`TabStop`. |
| override [GetHashCode](../../aspose.words/tabstop/gethashcode/)() | 计算该对象的哈希码。 |

## 评论

通常，制表位指定制表位存在的位置。但由于 制表位可以从父样式继承，因此子对象 可能需要显式定义给定位置没有制表位。要清除 给定位置处继承的制表位，请创建一个`TabStop`对象和 set [`Alignment`](./alignment/)到Clear。

欲了解更多信息，请参阅[`TabStopCollection`](../tabstopcollection/)。

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
