---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words for .NET
description: Aspose.Words.Math.OfficeMathJustification enum. Specifies the justification of the equation in C#.
type: docs
weight: 4280
url: /net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Specifies the justification of the equation.

```csharp
public enum OfficeMathJustification
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| CenterGroup | `1` | Justifies instances of mathematical text to the left with respect to each other, and centers the group of mathematical text (the Math Paragraph) with respect to the page. |
| Center | `2` | Centers each instance of mathematical text individually with respect to margins. |
| Left | `3` | Left justification of Math Paragraph. |
| Right | `4` | Right Justification of Math Paragraph. |
| Inline | `7` | Inline position of Math. |
| Default | `1` | Default value CenterGroup. |

## Examples

Shows how to set office math display formatting.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Change the location and display type of the OfficeMath node.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### See Also

* namespace [Aspose.Words.Math](../../aspose.words.math/)
* assembly [Aspose.Words](../../)
