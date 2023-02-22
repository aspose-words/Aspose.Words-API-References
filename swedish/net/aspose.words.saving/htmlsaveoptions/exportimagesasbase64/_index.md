---
title: HtmlSaveOptions.ExportImagesAsBase64
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger om bilder sparas i Base64format till utdata HTML MHTML eller EPUB. Standard ärfalsk .
type: docs
weight: 180
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportimagesasbase64/
---
## HtmlSaveOptions.ExportImagesAsBase64 property

Anger om bilder sparas i Base64-format till utdata HTML, MHTML eller EPUB. Standard är`falsk` .

```csharp
public bool ExportImagesAsBase64 { get; set; }
```

### Anmärkningar

När den här egenskapen är inställd på`Sann`bilddata exporteras direkt till **img** element och separata filer skapas inte.

### Exempel

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

Visar hur man sparar ett .html-dokument med bilder inbäddade i det.

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
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


