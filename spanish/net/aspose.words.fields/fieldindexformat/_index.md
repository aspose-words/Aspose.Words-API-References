---
title: FieldIndexFormat Enum
linktitle: FieldIndexFormat
articleTitle: FieldIndexFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.FieldIndexFormat para personalizar el formato FieldIndex en sus documentos. ¡Mejore la estructura de sus documentos fácilmente!
type: docs
weight: 2480
url: /es/net/aspose.words.fields/fieldindexformat/
---
## FieldIndexFormat enumeration

Especifica el formato para el[`FieldIndex`](../fieldindex/) campos en un documento.

```csharp
public enum FieldIndexFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Template | `0` | De plantilla. |
| Classic | `1` | Clásico. |
| Fancy | `2` | Elegante. |
| Modern | `3` | Moderno. |
| Bulleted | `4` | Con viñetas. |
| Formal | `5` | Formal. |
| Simple | `6` | Simple. |

## Ejemplos

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

* espacio de nombres [Aspose.Words.Fields](../../aspose.words.fields/)
* asamblea [Aspose.Words](../../)
