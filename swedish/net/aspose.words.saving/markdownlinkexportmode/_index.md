---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words för .NET
description: Upptäck hur Aspose.Words MarkdownLinkExportMode-enum förbättrar länkexport i Markdown och optimerar din dokumentkonverteringsprocess utan ansträngning.
type: docs
weight: 6030
url: /sv/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

Anger hur länkar exporteras till Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### Värderingar

| namn | Värde | Beskrivning |
| --- | --- | --- |
| Auto | `0` | Identifierar automatiskt exportläge för varje länk. |
| Inline | `1` | Exportera alla länkar som inbäddade block. |
| Reference | `2` | Exportera alla länkar som referensblock. |

## Exempel

Visar hur länkar skrivs till .md-filen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// Bilden kommer att skrivas som referens:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// Bilden kommer att skrivas som inline:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### Se även

* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
