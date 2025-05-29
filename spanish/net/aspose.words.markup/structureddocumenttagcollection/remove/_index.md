---
title: StructuredDocumentTagCollection.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words para .NET
description: Elimine sin esfuerzo etiquetas de documentos estructurados específicos utilizando el método StructuredDocumentTagCollection Remove para una gestión optimizada de documentos.
type: docs
weight: 70
url: /es/net/aspose.words.markup/structureddocumenttagcollection/remove/
---
## StructuredDocumentTagCollection.Remove method

Elimina la etiqueta del documento estructurado con el identificador especificado.

```csharp
public void Remove(int id)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| id | Int32 | El identificador de etiqueta de documento estructurado. |

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

* class [StructuredDocumentTagCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
