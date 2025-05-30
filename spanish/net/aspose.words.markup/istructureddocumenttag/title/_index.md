---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words para .NET
description: Descubra la propiedad Título de IStructuredDocumentTag defina un nombre intuitivo para su SDT y mejore la claridad del documento. ¡Obtenga más información ahora!
type: docs
weight: 140
url: /es/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Especifica el nombre descriptivo asociado con este**TED** . No puede ser nulo.

```csharp
public string Title { get; set; }
```

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

* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
