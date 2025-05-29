---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words för .NET
description: Omvandla former med EquationXML till Office Math-objekt utan ansträngning med hjälp av LoadOptions ConvertShapeToOfficeMath-egenskap för förbättrad dokumenttydlighet.
type: docs
weight: 40
url: /sv/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Hämtar eller anger om former ska konverteras med EquationXML till Office Math-objekt.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Exempel

Visar hur man konverterar EquationXML-former till Office Math-objekt.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Använd den här flaggan för att ange om formerna ska konverteras med EquationXML-attribut
// till Office Math-objekt och sedan ladda dokumentet.
loadOptions.ConvertShapeToOfficeMath = isConvertShapeToOfficeMath;

Document doc = new Document(MyDir + "Math shapes.docx", loadOptions);

if (isConvertShapeToOfficeMath)
{
    Assert.AreEqual(16, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(34, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
else
{
    Assert.AreEqual(24, doc.GetChildNodes(NodeType.Shape, true).Count);
    Assert.AreEqual(0, doc.GetChildNodes(NodeType.OfficeMath, true).Count);
}
```

### Se även

* class [LoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
