---
title: "Enum Aspose::Words::Saving::HtmlMetafileFormat"
linktitle: "HtmlMetafileFormat"
second_title: "Riferimento API Aspose.Words per C++"
description: "Enum Aspose::Words::Saving::HtmlMetafileFormat. Indica il formato in cui i metafili vengono salvati nei documenti HTML in C++."
type: docs
weight: 60000
url: /it/cpp/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enum


Indica il formato in cui i metafili vengono salvati nei documenti HTML.

```cpp
enum class HtmlMetafileFormat
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Png | 0 | I metafili vengono renderizzati in immagini raster PNG. |
| Svg | 1 | I metafili vengono convertiti in immagini vettoriali SVG. |
| EmfOrWmf | 2 | I metafili vengono salvati così come sono, senza conversione. |


## Esempi



Mostra come convertire gli oggetti SVG in un formato diverso durante il salvataggio dei documenti HTML.
```cpp
System::String html = u"<html>\r\n                    <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>\r\n                        <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>\r\n                    </svg>\r\n                </html>";

// Usa 'ConvertSvgToEmf' per ripristinare il comportamento legacy
// dove tutte le immagini SVG caricate da un documento HTML venivano convertite in EMF.
// Ora le immagini SVG vengono caricate senza conversione
// se la versione di MS Word specificata nelle opzioni di caricamento supporta nativamente le immagini SVG.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::HtmlLoadOptions>();
loadOptions->set_ConvertSvgToEmf(true);

auto doc = System::MakeObject<Aspose::Words::Document>(System::MakeObject<System::IO::MemoryStream>(System::Text::Encoding::get_UTF8()->GetBytes(html)), loadOptions);

// Questo documento contiene un elemento <svg> sotto forma di testo.
// Quando salviamo il documento in HTML, possiamo passare un oggetto SaveOptions
// per determinare come l'operazione di salvataggio gestisce questo oggetto.
// Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.Png" per convertirla in un'immagine PNG.
// Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.Svg" per conservarla come oggetto SVG.
// Impostare la proprietà "MetafileFormat" su "HtmlMetafileFormat.EmfOrWmf" per convertirla in un metafile.
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

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
