---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words per .NET
description: Scopri come Aspose.Words gestisce i paragrafi vuoti nell'esportazione in Markdown. Controlla la formattazione con l'enumerazione MarkdownEmptyParagraphExportMode.
type: docs
weight: 6010
url: /it/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Specifica come Aspose.Words esporta i paragrafi vuoti in Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| EmptyLine | `0` | Esporta come righe vuote. |
| MarkdownHardLineBreak | `1` | Esporta come carattere Markdown HardLineBreak '\'. |
| None | `2` | Non esportare paragrafi vuoti. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
