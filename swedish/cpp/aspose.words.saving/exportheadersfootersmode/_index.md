---
title: "Aspose::Words::Saving::ExportHeadersFootersMode enum"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::ExportHeadersFootersMode enum. Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB i C++."
type: docs
weight: 55000
url: /sv/cpp/aspose.words.saving/exportheadersfootersmode/
---
## ExportHeadersFootersMode enum


Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB.

```cpp
enum class ExportHeadersFootersMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| None | 0 | Sidhuvuden och sidfötter exporteras inte. |
| PerSection | 1 | Primära sidhuvuden och sidfötter exporteras i början och i slutet av varje sektion. |
| FirstSectionHeaderLastSectionFooter | 2 | Det primära sidhuvudet i den första sektionen exporteras i början av dokumentet och den primära sidfoten i slutet. |
| FirstPageHeaderFooterPerSection | 3 | Första sidhuvudet och sidfoten exporteras i början och i slutet av varje sektion. |


## Exempel



Visar hur man utelämnar sidhuvuden/sidfötter när man sparar ett dokument till HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Header and footer types.docx");

// Detta dokument innehåller sidhuvuden och sidfötter. Vi kan komma åt dem via samlingen \"HeadersFooters\".
ASSERT_EQ(u"First header", doc->get_FirstSection()->get_HeadersFooters()->idx_get(Aspose::Words::HeaderFooterType::HeaderFirst)->GetText().Trim());

// Format som .html delar inte upp dokumentet i sidor, så sidhuvuden/sidfötter kommer inte att fungera på samma sätt.
// som de skulle göra när vi öppnar dokumentet som en .docx med Microsoft Word.
// Om vi konverterar ett dokument med sidhuvuden/sidfötter till html, kommer konverteringen att integrera sidhuvuden/sidfötter i brödtexten.
// Vi kan använda ett SaveOptions-objekt för att utelämna sidhuvuden/sidfötter vid konvertering till html.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
saveOptions->set_ExportHeadersFootersMode(Aspose::Words::Saving::ExportHeadersFootersMode::None);

doc->Save(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html", saveOptions);

// Öppna vårt sparade dokument och verifiera att det inte innehåller sidhuvudets text
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"HeaderFooter.ExportMode.html");

ASSERT_FALSE(doc->get_Range()->get_Text().Contains(u"First header"));
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
