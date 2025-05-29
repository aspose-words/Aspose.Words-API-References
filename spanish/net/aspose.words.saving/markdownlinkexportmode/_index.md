---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words para .NET
description: Descubra cómo la enumeración Aspose.Words MarkdownLinkExportMode mejora la exportación de enlaces en Markdown, optimizando su proceso de conversión de documentos sin esfuerzo.
type: docs
weight: 6030
url: /es/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Especifica cómo se exportan los enlaces a Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Auto | `0` | Detectar automáticamente el modo de exportación para cada enlace. |
| Inline | `1` | Exportar todos los enlaces como bloques en línea. |
| Reference | `2` | Exportar todos los enlaces como bloques de referencia. |

## Ejemplos

Muestra cómo se escribirán los enlaces en el archivo .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

//La imagen se escribirá como referencia:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// La imagen se escribirá en línea:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
