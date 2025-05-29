---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words per .NET
description: Configura l'esportazione di paragrafi vuoti in Markdown con Aspose.Words. Imposta EmptyParagraphExportMode per una conversione ottimale del documento.
type: docs
weight: 20
url: /it/net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Specifica come esportare i paragrafi vuoti in Markdown. Il valore predefinito èEmptyLine .

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

## Esempi

Mostra come esportare paragrafi vuoti.

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

### Guarda anche

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
