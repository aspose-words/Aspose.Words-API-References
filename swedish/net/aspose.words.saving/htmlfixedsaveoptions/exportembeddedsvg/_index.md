---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words för .NET
description: HtmlFixedSaveOptions ExportEmbeddedSvg fast egendom. Anger om SVGresurser ska bäddas in i HTMLdokument. Standardvärdet ärSann  i C#.
type: docs
weight: 70
url: /sv/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Anger om SVG-resurser ska bäddas in i HTML-dokument. Standardvärdet är`Sann` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Exempel

Visar hur man bestämmer var SVG-objekt ska lagras när ett dokument exporteras till HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// När vi exporterar ett dokument med SVG-objekt till .html,
// Aspose.Words kan placera dessa objekt på två möjliga platser.
// Om du ställer in "ExportEmbeddedSvg"-flaggan till "true" kommer alla rådata från SVG-objektet att bäddas in
// inom utdata-HTML, inuti <bild> taggar.
// Om du ställer in denna flagga på "false" skapas en fil i det lokala filsystemet för varje SVG-objekt.
// HTML-koden länkar till varje fil med hjälp av "data"-attributet för ett <objekt> märka.
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
