---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words for .NET
description: Learn how Aspose.Words handles empty paragraphs in Markdown export. Control formatting with MarkdownEmptyParagraphExportMode enum.
type: docs
weight: 6010
url: /net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

Specifies how Aspose.Words exports empty paragraphs to Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| EmptyLine | `0` | Export as empty lines. |
| MarkdownHardLineBreak | `1` | Export as Markdown HardLineBreak character '\'. |
| None | `2` | Don't export empty paragraphs. |

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

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
