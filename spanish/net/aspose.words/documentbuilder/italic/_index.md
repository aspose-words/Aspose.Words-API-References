---
title: DocumentBuilder.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words para .NET
description: Descubra la propiedad cursiva de DocumentBuilder. Formatee fácilmente su texto en cursiva para mejorar la legibilidad y el estilo de sus documentos.
type: docs
weight: 140
url: /es/net/aspose.words/documentbuilder/italic/
---
## DocumentBuilder.Italic property

Verdadero si la fuente está formateada como cursiva.

```csharp
public bool Italic { get; set; }
```

## Ejemplos

Muestra cómo llenar campos MERGEFIELD con datos con un generador de documentos en lugar de una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar algunos MERGEFIELDS, que aceptan datos de columnas del mismo nombre en una fuente de datos durante una combinación de correspondencia,
// y luego rellenarlos manualmente.
builder.InsertField(" MERGEFIELD Chairman ");
builder.InsertField(" MERGEFIELD ChiefFinancialOfficer ");
builder.InsertField(" MERGEFIELD ChiefTechnologyOfficer ");

builder.MoveToMergeField("Chairman");
builder.Bold = true;
builder.Writeln("John Doe");

builder.MoveToMergeField("ChiefFinancialOfficer");
builder.Italic = true;
builder.Writeln("Jane Doe");

builder.MoveToMergeField("ChiefTechnologyOfficer");
builder.Italic = true;
builder.Writeln("John Bloggs");

doc.Save(ArtifactsDir + "DocumentBuilder.FillMergeFields.docx");
```

### Ver también

* class [DocumentBuilder](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
