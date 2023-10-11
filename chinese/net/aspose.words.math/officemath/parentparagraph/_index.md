---
title: OfficeMath.ParentParagraph
second_title: Aspose.Words for .NET API 参考
description: OfficeMath 财产. 检索父级Paragraph此节点的.
type: docs
weight: 50
url: /zh/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

检索父级[`Paragraph`](../../../aspose.words/paragraph/)此节点的.

```csharp
public Paragraph ParentParagraph { get; }
```

### 例子

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../officemath/)
* 部件 [Aspose.Words](../../../)


