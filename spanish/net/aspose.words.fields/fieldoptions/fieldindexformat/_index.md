---
title: FieldOptions.FieldIndexFormat
second_title: Referencia de API de Aspose.Words para .NET
description: FieldOptions propiedad. Obtiene o establece unFieldIndexFormat que representa el formato para elFieldIndex campos en el documento.
type: docs
weight: 90
url: /es/net/aspose.words.fields/fieldoptions/fieldindexformat/
---
## FieldOptions.FieldIndexFormat property

Obtiene o establece un`FieldIndexFormat` que representa el formato para el[`FieldIndex`](../../fieldindex/) campos en el documento.

```csharp
public FieldIndexFormat FieldIndexFormat { get; set; }
```

### Ejemplos

Muestra cómo formatear los campos FieldIndex.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("A");
builder.InsertBreak(BreakType.LineBreak);
builder.InsertField("XE \"A\"");
builder.Write("B");

builder.InsertField(" INDEX \\e \" · \" \\h \"A\" \\c \"2\" \\z \"1033\"", null);

doc.FieldOptions.FieldIndexFormat = FieldIndexFormat.Fancy;
doc.UpdateFields();

doc.Save(ArtifactsDir + "Field.SetFieldIndexFormat.docx");
```

### Ver también

* enum [FieldIndexFormat](../../fieldindexformat/)
* class [FieldOptions](../)
* espacio de nombres [Aspose.Words.Fields](../../fieldoptions/)
* asamblea [Aspose.Words](../../../)


