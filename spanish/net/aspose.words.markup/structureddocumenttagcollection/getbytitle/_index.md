---
title: StructuredDocumentTagCollection.GetByTitle
linktitle: GetByTitle
articleTitle: GetByTitle
second_title: Aspose.Words para .NET
description: Descubra el método GetByTitle en StructuredDocumentTagCollection, que recupera de manera eficiente la primera etiqueta de documento por título para una gestión de datos optimizada.
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

## Observaciones

Devuelve nulo si no se puede encontrar la etiqueta del documento estructurado con el título especificado.

## Ejemplos

Muestra cómo obtener la etiqueta de documento estructurado.

```csharp
Document doc = new Document(MyDir + "Structured document tags by id.docx");

// Obtener la etiqueta del documento estructurado por Id.
IStructuredDocumentTag sdt = doc.Range.StructuredDocumentTags.GetById(1160505028);
Console.WriteLine(sdt.IsMultiSection);
Console.WriteLine(sdt.Title);

// Obtener la etiqueta del documento estructurado o la etiqueta de rango por título.
sdt = doc.Range.StructuredDocumentTags.GetByTitle("Alias4");
Console.WriteLine(sdt.Id);
```

### Ver también

* interface [IStructuredDocumentTag](../../istructureddocumenttag/)
* class [StructuredDocumentTagCollection](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
