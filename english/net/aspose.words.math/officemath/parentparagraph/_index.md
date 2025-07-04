---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words for .NET
description: Discover the OfficeMath ParentParagraph property to easily access the parent Paragraph of any node, enhancing your document formatting and structure.
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

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath nodes that are children of other OfficeMath nodes are always inline.
// The node we are working with is the base node to change its location and display type.
Assert.That(officeMath.MathObjectType, Is.EqualTo(MathObjectType.OMathPara));
Assert.That(officeMath.NodeType, Is.EqualTo(NodeType.OfficeMath));
Assert.That(officeMath.ParentParagraph, Is.EqualTo(officeMath.ParentNode));

// Change the location and display type of the OfficeMath node.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### See Also

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* namespace [Aspose.Words.Math](../../../aspose.words.math/)
* assembly [Aspose.Words](../../../)
