---
title: HtmlSaveOptions.ExportImagesAsBase64
linktitle: ExportImagesAsBase64
articleTitle: ExportImagesAsBase64
second_title: Aspose.Words för .NET
description: Upptäck egenskapen HtmlSaveOptions ExportImagesAsBase64 för att spara bilder i Base64-format för optimerad HTML-, MHTML- eller EPUB-utdata. Förbättra din dokumentkvalitet!
type: docs
weight: 170
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Anger om bilder sparas i Base64-format som utdata i HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

## Anmärkningar

När den här egenskapen är inställd på`sann` bilddata exporteras direkt till**bild** element och separata filer skapas inte.

## Exempel

Visar hur man bäddar in teckensnitt i ett sparat HTML-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportFontsAsBase64 = true,
    CssStyleSheetType = CssStyleSheetType.Embedded,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

Visar hur man sparar ett .html-dokument med inbäddade bilder.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    ExportImagesAsBase64 = exportImagesAsBase64,
    PrettyFormat = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportImagesAsBase64.html");

Assert.True(exportImagesAsBase64
    ? outDocContents.Contains("<img src=\"data:image/png;base64")
    : outDocContents.Contains("<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```

### Se även

* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
