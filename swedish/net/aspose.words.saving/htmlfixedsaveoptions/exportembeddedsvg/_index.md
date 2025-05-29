---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words för .NET
description: Upptäck HtmlFixedSaveOptions ExportEmbeddedSvg-egenskap, bädda enkelt in SVG-resurser i dina HTML-dokument för förbättrad visuell presentation. Standardvärde: sant.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Anger om SVG-resurser ska bäddas in i HTML-dokumentet. Standardvärdet är`sann` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Exempel

Visar hur man avgör var SVG-objekt ska lagras när man exporterar ett dokument till HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// När vi exporterar ett dokument med SVG-objekt till .html,
// Aspose.Words kan placera dessa objekt på två möjliga platser.
// Om flaggan "ExportEmbeddedSvg" sätts till "true" bäddas all rådata för SVG-objektet in
// i utdata-HTML:en, inuti <image>-taggar.
// Om denna flagga sätts till "false" skapas en fil i det lokala filsystemet för varje SVG-objekt.
// HTML-koden länkar till varje fil med hjälp av attributet "data" i en <object>-tagg.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Se även

* class [HtmlFixedSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../../)
