---
title: MarkdownSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words för .NET
description: Optimera dina Markdown-exporter med egenskapen ImageResolution och ställ in anpassade utmatningsupplösningar för skarpare bilder. Standard, 96 dpi.
type: docs
weight: 60
url: /sv/net/aspose.words.saving/markdownsaveoptions/imageresolution/
---
## MarkdownSaveOptions.ImageResolution property

Anger utdataupplösningen för bilder vid export till Markdown. Standard är`96 dpi` .

```csharp
public int ImageResolution { get; set; }
```

## Exempel

Visar hur man ställer in upplösningen för bilder.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.ImageResolution = 300;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

### Se även

* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
