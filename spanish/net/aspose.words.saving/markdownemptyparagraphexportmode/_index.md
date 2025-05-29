---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words para .NET
description: Aprenda cómo Aspose.Words gestiona los párrafos vacíos en la exportación de Markdown. Controle el formato con la enumeración MarkdownEmptyParagraphExportMode.
type: docs
weight: 6010
url: /es/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Especifica cómo Aspose.Words exporta párrafos vacíos a Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| EmptyLine | `0` | Exportar como líneas vacías. |
| MarkdownHardLineBreak | `1` | Exportar como carácter Markdown HardLineBreak '\'. |
| None | `2` | No exportar párrafos vacíos. |

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
