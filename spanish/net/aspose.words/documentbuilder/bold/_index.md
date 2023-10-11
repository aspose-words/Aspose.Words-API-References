---
title: DocumentBuilder.Bold
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentBuilder propiedad. Verdadero si la fuente tiene el formato negrita.
type: docs
weight: 20
url: /es/net/aspose.words/documentbuilder/bold/
---
## DocumentBuilder.Bold property

Verdadero si la fuente tiene el formato negrita.

```csharp
public bool Bold { get; set; }
```

### Ejemplos

Muestra cómo llenar MERGEFIELD con datos con un generador de documentos en lugar de una combinación de correspondencia.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Insertar algunos MERGEFIELDS, que aceptan datos de columnas del mismo nombre en una fuente de datos durante una combinación de correspondencia,
// y luego llenarlos manualmente.
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
* espacio de nombres [Aspose.Words](../../documentbuilder/)
* asamblea [Aspose.Words](../../../)


