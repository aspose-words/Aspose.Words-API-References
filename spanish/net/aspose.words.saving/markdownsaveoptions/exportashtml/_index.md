---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words para .NET
description: Descubre cómo la propiedad MarkdownSaveOptions ExportAsHtml te permite personalizar elementos HTML para una exportación a Markdown fluida. ¡Maximiza la versatilidad de tu contenido!
type: docs
weight: 30
url: /es/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar. El valor predeterminado esNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

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

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
