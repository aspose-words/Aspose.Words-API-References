---
title: MarkdownSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words för .NET
description: MarkdownSaveOptions ExportImagesAsBase64 fast egendom. Anger om bilder sparas i Base64format till utdatafilen. Standardvärdet ärfalsk  i C#.
type: docs
weight: 20
url: /sv/net/aspose.words.saving/markdownsaveoptions/exportimagesasbase64/
---
## MarkdownSaveOptions.ExportImagesAsBase64 property

Anger om bilder sparas i Base64-format till utdatafilen. Standardvärdet är`falsk` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`Sann` bilddata exporteras direkt till**img** element och separata filer skapas inte.

## Exempel

Visar hur man sparar ett .md-dokument med bilder inbäddade i det.

```csharp
Document doc = new Document(MyDir + "Images.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions { ExportImagesAsBase64 = exportImagesAsBase64 };

doc.Save(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.ExportImagesAsBase64.md");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("data:image/jpeg;base64")
    : outDocContents.Contains("MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

### Se även

* class [MarkdownSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
