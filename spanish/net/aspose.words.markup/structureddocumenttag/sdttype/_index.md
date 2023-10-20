---
title: StructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words para .NET
description: StructuredDocumentTag SdtType propiedad. Obtiene el tipo de estoEtiqueta de documento estructurado  en C#.
type: docs
weight: 250
url: /es/net/aspose.words.markup/structureddocumenttag/sdttype/
---
## StructuredDocumentTag.SdtType property

Obtiene el tipo de esto**Etiqueta de documento estructurado** .

```csharp
public SdtType SdtType { get; }
```

## Ejemplos

Muestra cómo obtener el tipo de etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

List<StructuredDocumentTag> tags = doc.GetChildNodes(NodeType.StructuredDocumentTag, true)
    .OfType<StructuredDocumentTag>().ToList();

Assert.AreEqual(SdtType.RepeatingSection, tags[0].SdtType);
Assert.AreEqual(SdtType.RepeatingSectionItem, tags[1].SdtType);
Assert.AreEqual(SdtType.RichText, tags[2].SdtType);
```

### Ver también

* enum [SdtType](../../sdttype/)
* class [StructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
