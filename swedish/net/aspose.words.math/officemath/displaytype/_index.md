---
title: OfficeMath.DisplayType
second_title: Aspose.Words för .NET API Referens
description: OfficeMath fast egendom. Hämtar/ställer in Office Math visningsformattyp som representerar om en ekvation visas inline med texten eller visas på sin egen rad.
type: docs
weight: 10
url: /sv/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Hämtar/ställer in Office Math visningsformattyp som representerar om en ekvation visas inline med texten eller visas på sin egen rad.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Anmärkningar

Visningsformattyp har endast effekt för Office Math på högsta nivån.

Returnerad visningsformattyp är alltidInline för kapslad Office Math.

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

// OOXML- och WML-format använder egenskapen "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Ändra plats och visningstyp för OfficeMath-noden.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Se även

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../officemath/)
* hopsättning [Aspose.Words](../../../)


