---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words för .NET
description: Lär dig hur Aspose.Words hanterar tomma stycken i Markdown-export. Styr formatering med MarkdownEmptyParagraphExportMode-enum.
type: docs
weight: 6010
url: /sv/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Anger hur Aspose.Words exporterar tomma stycken till Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| EmptyLine | `0` | Exportera som tomma rader. |
| MarkdownHardLineBreak | `1` | Exportera som Markdown HardLineBreak-tecken '\'. |
| None | `2` | Exportera inte tomma stycken. |

## Exempel

Visar hur man exporterar tomma stycken.

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

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
