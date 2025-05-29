---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words för .NET
description: Konfigurera export av tomma stycken i Markdown med Aspose.Words. Ställ in EmptyParagraphExportMode för optimal dokumentkonvertering.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Anger hur tomma stycken ska exporteras till Markdown. Standardvärdet ärEmptyLine .

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

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

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
