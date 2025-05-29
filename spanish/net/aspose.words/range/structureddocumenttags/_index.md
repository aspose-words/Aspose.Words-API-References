---
title: Range.StructuredDocumentTags
linktitle: StructuredDocumentTags
articleTitle: StructuredDocumentTags
second_title: Aspose.Words para .NET
description: Descubra la propiedad Range StructuredDocumentTags, que proporciona una colección completa de etiquetas de documentos estructurados, mejorando la organización y la funcionalidad de su documento.
type: docs
weight: 50
url: /es/net/aspose.words/range/structureddocumenttags/
---
## Range.StructuredDocumentTags property

Devuelve un`StructuredDocumentTags` colección que representa todas las etiquetas de documentos estructurados en el rango.

```csharp
public StructuredDocumentTagCollection StructuredDocumentTags { get; }
```

## Ejemplos

Muestra cómo eliminar la etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

StructuredDocumentTagCollection structuredDocumentTags = doc.Range.StructuredDocumentTags;
IStructuredDocumentTag sdt;
for (int i = 0; i < structuredDocumentTags.Count; i++)
{
    sdt = structuredDocumentTags[i];
    Console.WriteLine(sdt.Title);
}

sdt = structuredDocumentTags.GetById(1691867797);
Assert.AreEqual(1691867797, sdt.Id);

Assert.AreEqual(5, structuredDocumentTags.Count);
//Eliminar la etiqueta del documento estructurado por Id.
structuredDocumentTags.Remove(1691867797);
//Eliminar la etiqueta del documento estructurado en la posición 0.
structuredDocumentTags.RemoveAt(0);
Assert.AreEqual(3, structuredDocumentTags.Count);
```

### Ver también

* class [StructuredDocumentTagCollection](../../../aspose.words.markup/structureddocumenttagcollection/)
* class [Range](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
