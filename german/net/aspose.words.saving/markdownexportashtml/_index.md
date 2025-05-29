---
title: MarkdownExportAsHtml Enum
linktitle: MarkdownExportAsHtml
articleTitle: MarkdownExportAsHtml
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Saving.MarkdownExportAsHtml, um Markdown-Elemente mühelos in reines HTML zu konvertieren und so Ihre Dokumentexportoptionen zu verbessern.
type: docs
weight: 6020
url: /de/net/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enumeration

Ermöglicht die Angabe der Elemente, die als reines HTML nach Markdown exportiert werden sollen.

```csharp
[Flags]
public enum MarkdownExportAsHtml
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Exportieren Sie alle Elemente mit Markdown-Syntax ohne reines HTML. |
| Tables | `1` | Tabellen als reines HTML exportieren. |

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

* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
