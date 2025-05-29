---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words pour .NET
description: Transformez sans effort des formes avec EquationXML en objets Office Math à l'aide de la propriété ConvertShapeToOfficeMath de LoadOptions pour une clarté de document améliorée.
type: docs
weight: 40
url: /fr/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Obtient ou définit s'il faut convertir les formes avec EquationXML en objets Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Exemples

Montre comment convertir des formes EquationXML en objets Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Utilisez cet indicateur pour spécifier s'il faut convertir les formes avec des attributs EquationXML
// aux objets Office Math, puis chargez le document.
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

### Voir également

* class [LoadOptions](../)
* espace de noms [Aspose.Words.Loading](../../../aspose.words.loading/)
* Assemblée [Aspose.Words](../../../)
