---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words för .NET API Referens
description: OfficeMath fast egendom. Hämtar/ställer in en kodning som användes för att koda ekvationsXML om detta matematiska kontorsobjekt läses från ekvationsXML. Vi använder kodningen när vi sparar ett dokument för att skriva i samma kodning som det lästes.
type: docs
weight: 20
url: /sv/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Hämtar/ställer in en kodning som användes för att koda ekvations-XML, om detta matematiska kontorsobjekt läses från -ekvations-XML. Vi använder kodningen när vi sparar ett dokument för att skriva i samma kodning som det lästes.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

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

* class [OfficeMath](../)
* namnutrymme [Aspose.Words.Math](../../officemath/)
* hopsättning [Aspose.Words](../../../)


