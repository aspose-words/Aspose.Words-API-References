---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words för .NET
description: Upptäck egenskapen LinkExportMode i MarkdownSaveOptions för att styra länkformatering i utdatafiler. Optimera dina dokumentexporter utan ansträngning!
type: docs
weight: 100
url: /sv/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

Anger hur länkar ska skrivas till utdatafilen. Standardvärdet ärAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

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

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
