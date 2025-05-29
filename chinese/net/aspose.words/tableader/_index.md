---
title: TabLeader Enum
linktitle: TabLeader
articleTitle: TabLeader
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.TabLeader 枚举，定义选项卡的引线样式，增强项目中的文档格式和可读性。
type: docs
weight: 7040
url: /zh/net/aspose.words/tableader/
---
## TabLeader enumeration

指定制表符下显示的引出线的类型。

```csharp
public enum TabLeader
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 不显示引线。 |
| Dots | `1` | 引导线由点组成。 |
| Dashes | `2` | 引线由虚线组成。 |
| Line | `3` | 引线是一条单线。 |
| Heavy | `4` | 引线是一条粗线。 |
| MiddleDot | `5` | 引导线由中间点组成。 |

## 例子

展示如何为段落设置自定义制表位。

```csharp
Document doc = new Document();
Paragraph para = doc.FirstSection.Body.FirstParagraph;

// 如果我们处于此集合中没有制表位的段落中，
// 在 Microsoft Word 中，每次按下 Tab 键，光标就会跳动 36 点。
Assert.AreEqual(0, doc.FirstSection.Body.FirstParagraph.GetEffectiveTabStops().Length);

// 如果我们通过“视图”选项卡启用标尺，我们可以在 Microsoft Word 中添加自定义制表位。
// 此标尺上的每个单位是两个默认制表位，即 72 点。
// 我们可以像这样以编程方式添加自定义制表位。
TabStopCollection tabStops = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.TabStops;
tabStops.Add(72, TabAlignment.Left, TabLeader.Dots);
tabStops.Add(216, TabAlignment.Center, TabLeader.Dashes);
tabStops.Add(360, TabAlignment.Right, TabLeader.Line);

// 我们可以通过“视图”->“显示”->“标尺”启用标尺，在 Microsoft Word 中看到这些制表位。
Assert.AreEqual(3, para.GetEffectiveTabStops().Length);

// 我们添加的任何制表符都将利用标尺上的制表位，并且可能，
// 根据标签前导符的值，在标签出发点和到达点之间留一条线。
para.AppendChild(new Run(doc, "\tTab 1\tTab 2\tTab 3"));

doc.Save(ArtifactsDir + "Paragraph.TabStops.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
