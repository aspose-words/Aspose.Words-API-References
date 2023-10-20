---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: 用于 .NET 的 Aspose.Words
description: OfficeMath ParentParagraph 财产. 检索父级Paragraph这个节点的 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

检索父级[`Paragraph`](../../../aspose.words/paragraph/)这个节点的.

```csharp
public Paragraph ParentParagraph { get; }
```

## 例子

显示如何设置办公室数学显示格式。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// 作为其他 OfficeMath 节点的子节点的 OfficeMath 节点始终是内联的。
// 我们正在使用的节点是更改其位置和显示类型的基础节点。
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// OOXML 和 WML 格式使用“EquationXmlEncoding”属性。
Assert.IsNull(officeMath.EquationXmlEncoding);

// 更改 OfficeMath 节点的位置和显示类型。
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### 也可以看看

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
