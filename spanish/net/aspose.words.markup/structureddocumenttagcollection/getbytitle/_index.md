---
title: StructuredDocumentTagCollection.GetByTitle
second_title: Referencia de API de Aspose.Words para .NET
description: StructuredDocumentTagCollection método. Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado.
type: docs
weight: 50
url: /es/net/aspose.words.markup/structureddocumenttagcollection/getbytitle/
---
## StructuredDocumentTagCollection.GetByTitle method

Devuelve la primera etiqueta de documento estructurado encontrada en la colección con el título especificado.

```csharp
public IStructuredDocumentTag GetByTitle(string title)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| title | String | El título de la etiqueta del documento estructurado. |

### Observaciones

Devuelve nulo si no se puede encontrar la etiqueta del documento estructurado con el título especificado.

### Ejemplos

Muestra cómo obtener una etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Obtener la etiqueta del documento estructurado por Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsRanged());
Console.WriteLine(sdt.Title);

// Obtenga la etiqueta del documento estructurado o la etiqueta de rango por Título.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ver también

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../structureddocumenttagcollection/)
* asamblea [Aspose.Words](../../../)


