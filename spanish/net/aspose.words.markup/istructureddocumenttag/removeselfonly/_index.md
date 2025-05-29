---
title: IStructuredDocumentTag.RemoveSelfOnly
linktitle: RemoveSelfOnly
articleTitle: RemoveSelfOnly
second_title: Aspose.Words para .NET
description: Descubra el método IStructuredDocumentTag RemoveSelfOnly para eliminar sin esfuerzo un nodo SDT y conservar su contenido en su árbol de documentos.
type: docs
weight: 180
url: /es/net/aspose.words.markup/istructureddocumenttag/removeselfonly/
---
## IStructuredDocumentTag.RemoveSelfOnly method

Elimina únicamente este nodo SDT, pero conserva su contenido dentro del árbol del documento.

```csharp
public void RemoveSelfOnly()
```

## Ejemplos

Muestra cómo eliminar la etiqueta de documento estructurado, pero mantiene el contenido dentro.

```csharp
Document doc = new Document(MyDir + "Structured document tags.docx");

 // Esta colección proporciona una interfaz unificada para acceder a etiquetas estructuradas con y sin rango.
IEnumerable<IStructuredDocumentTag> sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(5, sdts.Count());

// Aquí podemos obtener nodos secundarios de la interfaz común de etiquetas estructuradas con rango y sin rango.
foreach (IStructuredDocumentTag sdt in sdts)
    if (sdt.GetChildNodes(NodeType.Any, false).Count > 0)
        sdt.RemoveSelfOnly();

sdts = doc.Range.StructuredDocumentTags.ToList();
Assert.AreEqual(0, sdts.Count());
```

### Ver también

* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
