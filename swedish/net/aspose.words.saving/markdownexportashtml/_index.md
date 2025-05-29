---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Saving.MarkdownExportAsHtml enum för att enkelt konvertera Markdown-element till rå HTML, vilket förbättrar dina exportalternativ för dokument.
type: docs
weight: 6020
url: /sv/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Gör det möjligt att ange de element som ska exporteras till Markdown som rå HTML.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| None | `0` | Exportera alla element med Markdown-syntax utan någon rå HTML. |
| Tables | `1` | Exportera tabeller som rå HTML. |

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

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
