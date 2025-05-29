---
title: MarkdownSaveOptions.ExportAsHtml
linktitle: ExportAsHtml
articleTitle: ExportAsHtml
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie Sie mit der Eigenschaft MarkdownSaveOptions ExportAsHtml HTML-Elemente für den nahtlosen Markdown-Export anpassen können. Maximieren Sie die Vielseitigkeit Ihrer Inhalte!
type: docs
weight: 30
url: /de/net/aspose.words.saving/markdownsaveoptions/exportashtml/
---
## MarkdownSaveOptions.ExportAsHtml property

Ermöglicht die Angabe der Elemente, die als reines HTML nach Markdown exportiert werden sollen. Der Standardwert istNone .

```csharp
public MarkdownExportAsHtml ExportAsHtml { get; set; }
```

## Beispiele

Zeigt, wie eine Tabelle als reines HTML nach Markdown exportiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Sample table:");

// Tabelle erstellen.
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

### Siehe auch

* enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* class [MarkdownSaveOptions](../)
* namensraum [Aspose.Words.Saving](../../../aspose.words.saving/)
* Montage [Aspose.Words](../../../)
