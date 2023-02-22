---
title: OfficeMath.NodeType
second_title: Aspose.Words for .NET API 参考
description: OfficeMath 财产. 返回 节点类型.OfficeMath.
type: docs
weight: 50
url: /zh/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

返回 **节点类型.OfficeMath**.

```csharp
public override NodeType NodeType { get; }
```

### 例子

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../officemath/)
* 部件 [Aspose.Words](../../../)


