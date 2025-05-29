---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words för .NET
description: Upptäck OfficeMath DisplayType-egenskapen för flexibel ekvationsformatering – välj mellan inbäddad eller fristående visning för förbättrad dokumenttydlighet.
type: docs
weight: 10
url: /sv/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Hämtar/ställer in visningsformattypen för Office Math som representerar om en ekvation visas inbäddad i texten eller visas på en egen rad.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Anmärkningar

Visningsformattypen gäller endast för Office Math på högsta nivå.

Returnerad visningsformattyp är alltidInline för kapslad Office Math.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../../aspose.words.math/)
* hopsättning [Aspose.Words](../../../)
