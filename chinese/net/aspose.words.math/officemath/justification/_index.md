---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: 用于 .NET 的 Aspose.Words
description: OfficeMath Justification 财产. 获取/设置 Office Math 理由 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

获取/设置 Office Math 理由。

```csharp
public OfficeMathJustification Justification { get; set; }
```

## 评论

无法将对齐方式设置为具有显示格式类型的 Office MathInline。

无法将内联对齐设置为具有显示格式类型的 Office MathDisplay。

相应的[`DisplayType`](../displaytype/)必须在设置 Office Math 对齐方式之前进行设置。

## 例子

演示如何设置 Office 数学显示格式。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// 作为其他 OfficeMath 节点子级的 OfficeMath 节点始终是内联的。
// 我们正在使用的节点是改变其位置和显示类型的基础节点。
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// 更改 OfficeMath 节点的位置和显示类型。
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### 也可以看看

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
