---
title: MarkdownSaveOptions.ExportUnderlineFormatting
linktitle: ExportUnderlineFormatting
articleTitle: ExportUnderlineFormatting
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad MarkdownSaveOptions ExportUnderlineFormatting mejora la exportación de texto. Controle fácilmente el formato del subrayado con esta configuración booleana.
type: docs
weight: 50
url: /es/net/aspose.words.saving/markdownsaveoptions/exportunderlineformatting/
---
## MarkdownSaveOptions.ExportUnderlineFormatting property

Obtiene o establece un valor booleano que indica si se debe exportar el formato de texto subrayado como una secuencia de dos caracteres más "++". El valor predeterminado es`FALSO` .

```csharp
public bool ExportUnderlineFormatting { get; set; }
```

## Ejemplos

Muestra cómo exportar el formato de subrayado como ++.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Underline = Underline.Single;
builder.Write("Lorem ipsum. Dolor sit amet.");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions() { ExportUnderlineFormatting = true };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
