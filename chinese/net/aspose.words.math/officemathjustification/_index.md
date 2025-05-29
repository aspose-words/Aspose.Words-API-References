---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Math.OfficeMathJustification 枚举，实现精确的公式对齐。使用最佳对齐选项，提升文档的清晰度。
type: docs
weight: 4830
url: /zh/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

指定方程的对齐方式。

```csharp
public enum OfficeMathJustification
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| CenterGroup | `1` | 将数学文本实例彼此向左对齐，并将数学 文本组（数学段落）相对于页面居中。 |
| Center | `2` | 将每个数学文本实例相对于边距单独居中。 |
| Left | `3` | 数学段落左对齐。 |
| Right | `4` | 数学段落右对齐。 |
| Inline | `7` | Math. 的内联位置 |
| Default | `1` | 默认值CenterGroup. |

## 例子

展示如何设置办公室数学显示格式。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// 作为其他 OfficeMath 节点的子节点的 OfficeMath 节点始终是内联的。
// 我们正在处理的节点是改变其位置和显示类型的基础节点。
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// 更改OfficeMath节点的位置和显示类型。
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Math](../../aspose.words.math/)
* 部件 [Aspose.Words](../../)
