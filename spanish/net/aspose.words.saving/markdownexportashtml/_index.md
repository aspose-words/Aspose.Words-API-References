---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.MarkdownExportAsHtml para convertir sin esfuerzo elementos Markdown a HTML sin formato, mejorando sus opciones de exportación de documentos.
type: docs
weight: 6020
url: /es/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `0` | Exportar todos los elementos utilizando la sintaxis Markdown sin ningún HTML sin formato. |
| Tables | `1` | Exportar tablas como HTML sin formato. |

## Ejemplos

Muestra cómo exportar una tabla a Markdown como HTML sin formato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

//Crear tabla.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
