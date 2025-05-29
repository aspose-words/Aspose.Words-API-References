---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words for .NET
description: 探索 OfficeMath Justification 属性，轻松自定义和设置 Office Math 对齐方式。轻松提升文档的呈现效果！
type: docs
weight: 20
url: /zh/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

获取/设置 Office Math 对齐。

```csharp
public OfficeMathJustification Justification { get; set; }
```

## 评论

无法将对齐方式设置为带有显示格式类型的 Office MathInline。

内联对齐无法设置为带有显示格式类型的 Office MathDisplay。

相应的[`DisplayType`](../displaytype/)在设置 Office Math 对齐之前必须先进行设置。

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* 命名空间 [Aspose.Words.Math](../../../aspose.words.math/)
* 部件 [Aspose.Words](../../../)
