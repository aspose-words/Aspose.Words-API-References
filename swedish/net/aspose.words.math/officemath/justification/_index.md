---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words för .NET
description: Upptäck OfficeMaths justeringsfunktion för att enkelt anpassa och ställa in din Office Math-justering. Förbättra presentationen av ditt dokument utan ansträngning!
type: docs
weight: 20
url: /sv/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Hämtar/ställer in Office Math-justering.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Anmärkningar

Justering kan inte ställas in på Office Math med visningsformattypenInline.

Inline-justering kan inte ställas in på Office Math med visningsformattypenDisplay.

Motsvarande[`DisplayType`](../displaytype/) måste ställas in innan Office Math-justering kan ställas in.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
