---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words para .NET
description: Configura la exportación de párrafos vacíos en Markdown con Aspose.Words. Configura EmptyParagraphExportMode para una conversión óptima del documento.
type: docs
weight: 20
url: /es/net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Especifica cómo exportar párrafos vacíos a Markdown. El valor predeterminado esEmptyLine .

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

## Ejemplos

Muestra cómo exportar párrafos vacíos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("First");
builder.Writeln("\r\n\r\n\r\n");
builder.Writeln("Last");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.EmptyParagraphExportMode = exportMode;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

string result = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case MarkdownEmptyParagraphExportMode.None:
        Assert.AreEqual("First\r\n\r\nLast\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.EmptyLine:
        Assert.AreEqual("First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.MarkdownHardLineBreak:
        Assert.AreEqual("First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;
}
```

### Ver también

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
