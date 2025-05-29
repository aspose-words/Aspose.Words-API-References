---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words för .NET
description: Upptäck HtmlLoadOptions egenskap ConvertSvgToEmf. Kontrollera enkelt konvertering av SVG till EMF för optimal bildkvalitet. Standardvärdet är falskt; behåll SVG:erna intakta!
type: docs
weight: 30
url: /sv/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Hämtar eller ställer in ett värde som anger om inlästa SVG-bilder ska konverteras till EMF-format. Standardvärdet är`falsk` och, om möjligt, lagras inlästa SVG-bilder som de är utan konvertering.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Anmärkningar

Nyare versioner av MS Word har stöd för SVG-bilder direkt. Om den MS Word-version som anges i laddningsalternativen stöder SVG, kommer Aspose.Words att lagra SVG-bilder som de är utan konvertering. Om SVG inte stöds kommer inlästa SVG-bilder att konverteras till EMF-format.

Om det här alternativet däremot är inställt på`sann` Aspose.Words konverterar inlästa SVG-bilder till EMF även om SVG -bilder stöds av den angivna versionen av MS Word.

## Exempel

Visar hur man konverterar SVG-objekt till ett annat format när man sparar HTML-dokument.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Använd 'ConvertSvgToEmf' för att återställa det äldre beteendet
// där alla SVG-bilder som laddats från ett HTML-dokument konverterades till EMF.
// Nu laddas SVG-bilder utan konvertering
// om MS Word-versionen som anges i laddningsalternativen har stöd för SVG-bilder.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// Detta dokument innehåller ett <svg>-element i textform.
// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att avgöra hur sparoperationen hanterar detta objekt.
// Ställer in egenskapen "MetafileFormat" till "HtmlMetafileFormat.Png" för att konvertera den till en PNG-bild.
// Om egenskapen "MetafileFormat" ställs in på "HtmlMetafileFormat.Svg" bevaras den som ett SVG-objekt.
// Ställer in egenskapen "MetafileFormat" till "HtmlMetafileFormat.EmfOrWmf" för att konvertera den till en metafil.
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
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
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

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
