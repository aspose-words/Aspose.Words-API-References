---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words för .NET
description: Upptäck OfficeMath ParentParagraph-egenskapen för att enkelt komma åt det överordnade stycket för valfri nod, vilket förbättrar formateringen och strukturen i ditt dokument.
type: docs
weight: 50
url: /sv/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Hämtar föräldern[`Paragraph`](../../../aspose.words/paragraph/) av denna nod.

```csharp
public Paragraph ParentParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
