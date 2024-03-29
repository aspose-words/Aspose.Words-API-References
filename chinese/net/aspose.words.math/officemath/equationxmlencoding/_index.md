---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words for .NET API 参考
description: OfficeMath 财产. 获取/设置用于对等式 XML 进行编码的编码如果此办公数学对象是从 等式 XML 读取的我们在保存文档时使用编码以与读取时相同的编码写入
type: docs
weight: 20
url: /zh/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

获取/设置用于对等式 XML 进行编码的编码，如果此办公数学对象是从 等式 XML 读取的。我们在保存文档时使用编码以与读取时相同的编码写入。

```csharp
public Encoding EquationXmlEncoding { get; set; }
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

* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../officemath/)
* 部件 [Aspose.Words](../../../)


