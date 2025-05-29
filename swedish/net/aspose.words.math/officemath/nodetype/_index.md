---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words för .NET
description: Upptäck OfficeMath NodeType-egenskapen som effektivt returnerar OfficeMath-element och förbättrar ditt dokuments matematiska funktioner.
type: docs
weight: 40
url: /sv/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

ReturerOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

## Exempel

Visar hur man ställer in formatering för Office-matematikvisning.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-noder som är underordnade till andra OfficeMath-noder är alltid inline.
// Noden vi arbetar med är basnoden för att ändra dess plats och visningstyp.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Ändra plats och visningstyp för OfficeMath-noden.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Se även

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
