---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words para .NET
description: Descubre la propiedad MarkdownSaveOptions LinkExportMode para controlar el formato de los enlaces en los archivos de salida. ¡Optimiza la exportación de tus documentos fácilmente!
type: docs
weight: 100
url: /es/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Especifica cómo se escribirán los enlaces en el archivo de salida. El valor predeterminado esAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

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

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
