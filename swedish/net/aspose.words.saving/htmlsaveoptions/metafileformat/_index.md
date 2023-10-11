---
title: HtmlSaveOptions.MetafileFormat
second_title: Aspose.Words för .NET API Referens
description: HtmlSaveOptions fast egendom. Anger i vilket format metafiler sparas vid export till HTML MHTML eller EPUB. Standardvärdet ärPng  vilket betyder att metafiler renderas till raster PNGbilder.
type: docs
weight: 380
url: /sv/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

Anger i vilket format metafiler sparas vid export till HTML, MHTML eller EPUB. Standardvärdet ärPng , vilket betyder att metafiler renderas till raster PNG-bilder.

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

### Anmärkningar

Metafiler visas inte av HTML-webbläsare. Som standard konverterar Aspose.Words WMF- och EMF -bilder till PNG-filer vid export till HTML. Andra alternativ är att konvertera metafiler till SVG-bilder eller att exportera dem som de är utan konvertering.

Vissa bildomvandlingar, särskilt bildbeskärning, kommer inte att tillämpas på metafilbilder om de exporteras till HTML utan konvertering.

### Exempel

Visar hur du konverterar SVG-objekt till ett annat format när du sparar HTML-dokument.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Använd 'ConvertSvgToEmf' för att återställa det äldre beteendet
// där alla SVG-bilder laddade från ett HTML-dokument konverterades till EMF.
// Nu laddas SVG-bilder utan konvertering
// om MS Word-versionen som anges i laddningsalternativ stöder SVG-bilder inbyggt.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Detta dokument innehåller en <svg> element i form av text.
// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur sparoperationen hanterar detta objekt.
// Ställ in egenskapen "MetafileFormat" till "HtmlMetafileFormat.Png" för att konvertera den till en PNG-bild.
// Genom att ställa in egenskapen "MetafileFormat" till "HtmlMetafileFormat.Svg" bevaras den som ett SVG-objekt.
// Ställ in egenskapen "MetafileFormat" till "HtmlMetafileFormat.EmfOrWmf" för att konvertera den till en metafil.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height= \"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Se även

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* namnutrymme [Aspose.Words.Saving](../../htmlsaveoptions/)
* hopsättning [Aspose.Words](../../../)


