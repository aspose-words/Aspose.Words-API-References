---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words for .NET
description: Aspose.Words.Math.OfficeMathDisplayType enum. Specifies the display format type of the equation in C#.
type: docs
weight: 4530
url: /net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Specifies the display format type of the equation.

```csharp
public enum OfficeMathDisplayType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Display | `0` | The Office Math is displayed on its own line. |
| Inline | `1` | The Office Math is displayed inline with the text. |

## Examples

Shows how to set office math display formatting.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

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
