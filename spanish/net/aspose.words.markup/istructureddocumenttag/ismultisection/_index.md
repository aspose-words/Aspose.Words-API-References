---
title: IStructuredDocumentTag.IsMultiSection
linktitle: IsMultiSection
articleTitle: IsMultiSection
second_title: Aspose.Words para .NET
description: Descubra la propiedad IsMultiSection de IStructuredDocumentTag, que identifica si su etiqueta es una multisección con rango, mejorando la organización y la funcionalidad del documento.
type: docs
weight: 40
url: /es/net/aspose.words.markup/istructureddocumenttag/ismultisection/
---
## IStructuredDocumentTag.IsMultiSection property

Devuelve verdadero si esta instancia es una etiqueta de documento estructurado de rango (varias secciones).

```csharp
public bool IsMultiSection { get; }
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
