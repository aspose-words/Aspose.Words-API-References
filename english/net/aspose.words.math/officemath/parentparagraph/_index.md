---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words for .NET
description: OfficeMath ParentParagraph property. Retrieves the parent Paragraph of this node in C#.
type: docs
weight: 50
url: /net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Retrieves the parent [`Paragraph`](../../../aspose.words/paragraph/) of this node.

```csharp
public Paragraph ParentParagraph { get; }
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* namespace [Aspose.Words.Math](../../officemath/)
* assembly [Aspose.Words](../../../)
