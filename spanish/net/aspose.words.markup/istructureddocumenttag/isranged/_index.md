---
title: IStructuredDocumentTag.IsRanged
linktitle: IsRanged
articleTitle: IsRanged
second_title: Aspose.Words para .NET
description: IStructuredDocumentTag IsRanged método. Devuelve verdadero si esta instancia es una etiqueta de documento estructurado por rangos en C#.
type: docs
weight: 140
url: /es/net/aspose.words.markup/istructureddocumenttag/isranged/
---
## IStructuredDocumentTag.IsRanged method

Devuelve verdadero si esta instancia es una etiqueta de documento estructurado por rangos.

```csharp
public bool IsRanged()
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
