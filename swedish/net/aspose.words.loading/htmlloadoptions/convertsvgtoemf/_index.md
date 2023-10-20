---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words för .NET
description: HtmlLoadOptions ConvertSvgToEmf fast egendom. Hämtar eller ställer in ett värde som anger om laddade SVGbilder ska konverteras till EMFformatet. Standardvärdet ärfalsk och om möjligt lagras inlästa SVGbilder som de är utan konvertering i C#.
type: docs
weight: 30
url: /sv/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Hämtar eller ställer in ett värde som anger om laddade SVG-bilder ska konverteras till EMF-formatet. Standardvärdet är`falsk` och om möjligt lagras inlästa SVG-bilder som de är utan konvertering.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Anmärkningar

Nyare versioner av MS Word stöder SVG-bilder inbyggt. Om MS Word-versionen som anges i laddningsalternativen stöder SVG, kommer Aspose.Words att lagra SVG-bilder som de är utan konvertering. Om SVG inte stöds kommer inlästa SVG-bilder att konverteras till EMF-formatet.

Om detta alternativ är satt till`Sann` , Aspose.Words kommer att konvertera laddade SVG-bilder till EMF även om SVG -bilder stöds av den angivna versionen av MS Word.

## Exempel

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

* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
