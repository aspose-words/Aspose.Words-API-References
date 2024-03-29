---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: 用于 .NET 的 Aspose.Words
description: OfficeMath DisplayType 财产. 获取/设置 Office Math 显示格式类型该类型表示方程是与文本 内联显示还是在其自己的行上显示 在 C#.
type: docs
weight: 10
url: /zh/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

获取/设置 Office Math 显示格式类型，该类型表示方程是与文本 内联显示还是在其自己的行上显示。

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## 评论

显示格式类型仅对顶级 Office Math 有效。

返回的显示格式类型始终是Inline用于嵌套 Office Math。

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
