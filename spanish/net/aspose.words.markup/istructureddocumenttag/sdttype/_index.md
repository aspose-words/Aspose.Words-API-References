---
title: IStructuredDocumentTag.SdtType
linktitle: SdtType
articleTitle: SdtType
second_title: Aspose.Words para .NET
description: Descubra la propiedad IStructuredDocumentTag SdtType para identificar fácilmente el tipo de etiquetas de documento estructurado para una mejor gestión de documentos.
type: docs
weight: 120
url: /es/net/aspose.words.markup/istructureddocumenttag/sdttype/
---
## IStructuredDocumentTag.SdtType property

Obtiene el tipo de esto**Etiqueta de documento estructurado** .

```csharp
public SdtType SdtType { get; }
```

## Ejemplos

Muestra cómo obtener el tipo de una etiqueta de documento estructurado.

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
* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
