---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words per .NET
description: Trasforma senza sforzo le forme con EquationXML in oggetti Office Math utilizzando la proprietà ConvertShapeToOfficeMath di LoadOptions, per una maggiore chiarezza del documento.
type: docs
weight: 40
url: /it/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Ottiene o imposta se convertire le forme con EquationXML in oggetti Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Esempi

Mostra come convertire le forme EquationXML in oggetti Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Utilizzare questo flag per specificare se convertire le forme con attributi EquationXML
// agli oggetti di Office Math e quindi carica il documento.
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

### Guarda anche

* class [LoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
