---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Math.OfficeMathDisplayType 枚举. 指定方程的显示格式类型 在 C#.
type: docs
weight: 4130
url: /zh/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

指定方程的显示格式类型。

```csharp
public enum OfficeMathDisplayType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Display | `0` | Office Math 显示在其自己的行上。 |
| Inline | `1` | Office Math 与文本内联显示。 |

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

* 命名空间 [Aspose.Words.Math](../../aspose.words.math/)
* 部件 [Aspose.Words](../../)
