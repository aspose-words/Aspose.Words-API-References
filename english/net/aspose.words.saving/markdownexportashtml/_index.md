---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Saving.MarkdownExportAsHtml enum to effortlessly convert Markdown elements to raw HTML, enhancing your document export options.
type: docs
weight: 6000
url: /net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Allows to specify the elements to be exported to Markdown as raw HTML.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | `0` | Export all elements using Markdown syntax without any raw HTML. |
| Tables | `1` | Export tables as raw HTML. |

## Examples

Shows how to export a table to Markdown as raw HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Create table.
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Right;
builder.Write("Cell1");
builder.InsertCell();
builder.ParagraphFormat.Alignment = ParagraphAlignment.Center;
builder.Write("Cell2");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ExportAsHtml = MarkdownExportAsHtml.Tables;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
