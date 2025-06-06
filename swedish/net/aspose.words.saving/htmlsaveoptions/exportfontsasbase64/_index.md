---
title: HtmlSaveOptions.ExportFontsAsBase64
linktitle: ExportFontsAsBase64
articleTitle: ExportFontsAsBase64
second_title: Aspose.Words för .NET
description: Upptäck hur egenskapen HtmlSaveOptions ExportFontsAsBase64 förbättrar din HTML genom att bädda in teckensnitt i Base64-kodning för förbättrad prestanda. Standardvärdet är falskt.
type: docs
weight: 150
url: /sv/net/aspose.words.saving/htmlsaveoptions/exportfontsasbase64/
---
## HtmlSaveOptions.ExportFontsAsBase64 property

Anger om teckensnittsresurser ska bäddas in i HTML i Base64-kodning. Standard är`falsk` .

```csharp
public bool ExportFontsAsBase64 { get; set; }
```

## Anmärkningar

Som standard skrivs teckensnitt till separata filer. Om det här alternativet är inställt på`sann`, teckensnitt kommer att bäddas in i dokumentets CSS i Base64-kodning.

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
