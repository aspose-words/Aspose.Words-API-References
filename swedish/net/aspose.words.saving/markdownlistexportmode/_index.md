---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words MarkdownListExportMode-enum förbättrar listexport till Markdown, vilket säkerställer exakt formatering och sömlös integration för dina dokument.
type: docs
weight: 6040
url: /sv/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

Anger hur listor exporteras till Markdown.

```csharp
public enum MarkdownListExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| MarkdownSyntax | `0` | Exportera listobjekt som är kompatibla med Markdown-syntax. |
| PlainText | `1` | Exportera listobjekt som vanlig text. |

## Exempel

Visar hur man listar objekt som kommer att skrivas till markdown-dokumentet.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// Använd MarkdownListExportMode.PlainText eller MarkdownListExportMode.MarkdownSyntax för att exportera listan.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
