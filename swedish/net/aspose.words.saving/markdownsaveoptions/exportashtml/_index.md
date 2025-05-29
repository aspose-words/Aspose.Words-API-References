---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen MarkdownSaveOptions ExportAsHtml låter dig anpassa HTML-element för sömlös Markdown-export. Maximera ditt innehålls mångsidighet!
type: docs
weight: 30
url: /sv/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Gör det möjligt att ange de element som ska exporteras till Markdown som rå HTML. Standardvärdet ärNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Exempel

Visar hur man exporterar en tabell till Markdown som rå HTML.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Skapa tabell.
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

### Se även

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
