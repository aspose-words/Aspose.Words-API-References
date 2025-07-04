---
title: MarkdownSaveOptions.EmptyParagraphExportMode
linktitle: EmptyParagraphExportMode
articleTitle: EmptyParagraphExportMode
second_title: Aspose.Words for .NET
description: Configure empty paragraph export in Markdown with Aspose.Words. Set EmptyParagraphExportMode for optimal document conversion.
type: docs
weight: 20
url: /net/aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/
---
## MarkdownSaveOptions.EmptyParagraphExportMode property

Specifies how to export empty paragraphs to Markdown. Default value is EmptyLine.

```csharp
public MarkdownEmptyParagraphExportMode EmptyParagraphExportMode { get; set; }
```

## Examples

Shows how to export empty paragraphs.

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
        Assert.That(result, Is.EqualTo("First\r\n\r\nLast\r\n"));
        break;
    case MarkdownEmptyParagraphExportMode.EmptyLine:
        Assert.That(result, Is.EqualTo("First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n"));
        break;
    case MarkdownEmptyParagraphExportMode.MarkdownHardLineBreak:
        Assert.That(result, Is.EqualTo("First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n"));
        break;
}
```

### See Also

* enum [MarkdownEmptyParagraphExportMode](../../markdownemptyparagraphexportmode/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
