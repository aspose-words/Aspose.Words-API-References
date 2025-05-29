---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words für .NET
description: Wandeln Sie Formen mit EquationXML mühelos in Office Math-Objekte um, indem Sie die ConvertShapeToOfficeMath-Eigenschaft von LoadOptions verwenden, um die Dokumentübersichtlichkeit zu verbessern.
type: docs
weight: 40
url: /de/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Ruft ab oder legt fest, ob Formen mit EquationXML in Office Math-Objekte konvertiert werden sollen.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Beispiele

Zeigt, wie EquationXML-Formen in Office Math-Objekte konvertiert werden.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Verwenden Sie dieses Flag, um anzugeben, ob die Formen mit EquationXML-Attributen konvertiert werden sollen
// zu Office Math-Objekten und laden Sie dann das Dokument.
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

### Siehe auch

* class [LoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
