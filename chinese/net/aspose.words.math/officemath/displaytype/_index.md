---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words for .NET
description: 探索 OfficeMath DisplayType 属性以实现灵活的公式格式 - 选择内联或独立显示以增强文档清晰度。
type: docs
weight: 10
url: /zh/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

获取/设置 Office Math 显示格式类型，表示公式是否与文本内联显示或显示在自己的行上。

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## 评论

显示格式类型仅对顶级 Office Math 有效。

返回的显示格式类型始终是Inline用于嵌套的 Office Math。

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
