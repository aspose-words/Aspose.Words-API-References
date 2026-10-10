---
title: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf metod"
linktitle: "get_ConvertSvgToEmf"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf metod. Hämtar eller anger ett värde som indikerar om inlästa SVG-bilder ska konverteras till EMF-formatet. Standardvärdet är falskt och, om möjligt, lagras inlästa SVG-bilder oförändrade utan konvertering i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.loading/htmlloadoptions/get_convertsvgtoemf/
---
## HtmlLoadOptions::get_ConvertSvgToEmf method


Hämtar eller anger ett värde som indikerar om inlästa SVG-bilder ska konverteras till EMF-format. Standardvärdet är **false** och, om möjligt, lagras inlästa SVG-bilder som de är utan konvertering.

```cpp
bool Aspose::Words::Loading::HtmlLoadOptions::get_ConvertSvgToEmf() const
```

## Anmärkningar


Nyare versioner av MS Word stöder SVG-bilder nativt. Om den MS Word-version som anges i laddningsalternativen stöder SVG, kommer Aspose.Words att lagra SVG-bilder oförändrade utan konvertering. Om SVG inte stöds, kommer inlästa SVG-bilder att konverteras till EMF-formatet.

Om, däremot, detta alternativ är satt till **true**, kommer Aspose.Words att konvertera inlästa SVG-bilder till EMF även om SVG-bilder stöds av den angivna versionen av MS Word.

## Exempel



Visar hur man konverterar SVG-objekt till ett annat format när HTML-dokument sparas.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Använd 'ConvertSvgToEmf' för att återgå till det äldre beteendet
// där alla SVG-bilder som laddats från ett HTML-dokument konverterades till EMF.
// Nu laddas SVG-bilder utan konvertering
// om den MS Word-version som anges i inläsningsalternativen stöder SVG-bilder nativt.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Det här dokumentet innehåller ett <svg>-element i form av text.
// När vi sparar dokumentet till HTML kan vi skicka ett SaveOptions-objekt
// för att bestämma hur sparningsoperationen hanterar detta objekt.
// Ställer in egenskapen "MetafileFormat" till "HtmlMetafileFormat.Png" för att konvertera den till en PNG-bild.
// Ställer in egenskapen "MetafileFormat" till "HtmlMetafileFormat.Svg" bevarar den som ett SVG-objekt.
// Ställer in egenskapen "MetafileFormat" till "HtmlMetafileFormat.EmfOrWmf" för att konvertera den till en metafil.
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_MetafileFormat(htmlMetafileFormat);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case Aspose::Words::Saving::HtmlMetafileFormat::Png:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::Svg:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">") + u"<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height=\"40\">"));
        break;

    case Aspose::Words::Saving::HtmlMetafileFormat::EmfOrWmf:
        ASSERT_TRUE(outDocContents.Contains(System::String(u"<p style=\"margin-top:0pt; margin-bottom:0pt\">") + u"<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " + u"style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>"));
        break;

}
```

## Se även

* Class [HtmlLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
