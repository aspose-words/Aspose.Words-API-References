---
title: IStructuredDocumentTag.Title
linktitle: Title
articleTitle: Title
second_title: Aspose.Words para .NET
description: IStructuredDocumentTag Title propiedad. Especifica el nombre descriptivo asociado con esteTED . No puede ser nulo en C#.
type: docs
weight: 110
url: /es/net/aspose.words.markup/istructureddocumenttag/title/
---
## IStructuredDocumentTag.Title property

Especifica el nombre descriptivo asociado con este**TED** . No puede ser nulo.

```csharp
public string Title { get; set; }
```

## Ejemplos

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

* interface [IStructuredDocumentTag](../)
* espacio de nombres [Aspose.Words.Markup](../../../aspose.words.markup/)
* asamblea [Aspose.Words](../../../)
