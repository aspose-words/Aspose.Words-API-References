---
title: OfficeMath.Justification
second_title: Aspose.Words för .NET API Referens
description: OfficeMath fast egendom. Får/ställer in Office Math motivering.
type: docs
weight: 20
url: /sv/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Får/ställer in Office Math motivering.

```csharp
public OfficeMathJustification Justification { get; set; }
```

### Anmärkningar

Justering kan inte ställas in på Office Math med visningsformattypInline.

Inline-justering kan inte ställas in på Office Math med visningsformattypDisplay.

Motsvarande[`DisplayType`](../displaytype/) måste ställas in innan du ställer in Office Math-motivering.

### Exempel

Visar hur du ställer in kontorsmattevisningsformatering.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// OfficeMath-noder som är barn till andra OfficeMath-noder är alltid inline.
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
* namnutrymme [Aspose.Words.Math](../../officemath/)
* hopsättning [Aspose.Words](../../../)


