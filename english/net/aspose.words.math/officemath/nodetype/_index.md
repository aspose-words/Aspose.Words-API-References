---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words for .NET API Reference
description: OfficeMath NodeType property. Returns OfficeMath in C#.
type: docs
weight: 40
url: /net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

Returns OfficeMath.

```csharp
public override NodeType NodeType { get; }
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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* namespace [Aspose.Words.Math](../../officemath/)
* assembly [Aspose.Words](../../../)
