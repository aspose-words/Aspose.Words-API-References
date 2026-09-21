---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode‑metod"
linktitle: "get_ExportHeadersFootersMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode‑metod. Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB. Standardvärdet är PerSection för HTML/MHTML och None för EPUB i C++."
type: docs
weight: 18000
url: /sv/cpp/aspose.words.saving/htmlsaveoptions/get_exportheadersfootersmode/
---
## HtmlSaveOptions::get_ExportHeadersFootersMode method


Anger hur sidhuvuden och sidfötter exporteras till HTML, MHTML eller EPUB. Standardvärdet är [PerSection](../../exportheadersfootersmode/) för HTML/MHTML och [None](../../exportheadersfootersmode/) för EPUB.

```cpp
Aspose::Words::Saving::ExportHeadersFootersMode Aspose::Words::Saving::HtmlSaveOptions::get_ExportHeadersFootersMode() const
```

## Anmärkningar


Det är svårt att meningsfullt exportera sidhuvuden och sidfötter till HTML eftersom HTML inte är paginerat.

När denna egenskap är [PerSection](../../exportheadersfootersmode/) exporterar Aspose.Words endast primära sidhuvuden och sidfötter i början och slutet av varje avsnitt.

När den är [FirstSectionHeaderLastSectionFooter](../../exportheadersfootersmode/) exporteras endast det första primära sidhuvudet och den sista primära sidfoten (inklusive länkade till föregående).

Du kan inaktivera export av sidhuvuden och sidfötter helt genom att ställa in den här egenskapen till [None](../../exportheadersfootersmode/).

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

* Enum [ExportHeadersFootersMode](../../exportheadersfootersmode/)
* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
