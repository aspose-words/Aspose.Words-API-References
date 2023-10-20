---
title: LoadOptions.ConvertShapeToOfficeMath
linktitle: ConvertShapeToOfficeMath
articleTitle: ConvertShapeToOfficeMath
second_title: Aspose.Words para .NET
description: LoadOptions ConvertShapeToOfficeMath propiedad. Obtiene o establece si se deben convertir formas con EquationXML en objetos de Office Math en C#.
type: docs
weight: 40
url: /es/net/aspose.words.loading/loadoptions/convertshapetoofficemath/
---
## LoadOptions.ConvertShapeToOfficeMath property

Obtiene o establece si se deben convertir formas con EquationXML en objetos de Office Math.

```csharp
public bool ConvertShapeToOfficeMath { get; set; }
```

## Ejemplos

Muestra cómo convertir formas EquationXML en objetos de Office Math.

```csharp
LoadOptions loadOptions = new LoadOptions();

// Utilice esta bandera para especificar si se deben convertir las formas con atributos de EquationXML
// a objetos de Office Math y luego carga el documento.
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

### Ver también

* class [LoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
