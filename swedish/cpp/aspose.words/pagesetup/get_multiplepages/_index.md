---
title: "Aspose::Words::PageSetup::get_MultiplePages metod"
linktitle: "get_MultiplePages"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_MultiplePages metod. För dokument med flera sidor, hämtar eller anger hur ett dokument skrivs ut eller renderas så att det kan bindas som en häfte i C++."
type: docs
weight: 29000
url: /sv/cpp/aspose.words/pagesetup/get_multiplepages/
---
## PageSetup::get_MultiplePages method


För dokument med flera sidor hämtas eller anges hur ett dokument skrivs ut eller renderas så att det kan bindas som en häfte.

```cpp
Aspose::Words::Settings::MultiplePagesType Aspose::Words::PageSetup::get_MultiplePages() const
```


## Exempel



Visar hur man ställer in mellanrumsmarginaler.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga text som sträcker sig över flera sidor.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
for (int32_t i = 0; i < 6; i++)
{
    builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, ") + u"sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Ett mellanrum lägger till vita utrymmen antingen på vänster eller höger sidmarginal,
// vilket kompenserar för den centrala vikningen av sidor i en bok som inkräktar på sidans layout.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

// Bestäm hur mycket utrymme våra sidor har för text inom marginalerna och lägg sedan till ett belopp för att fylla ut en marginal.
ASSERT_NEAR(470.30, pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin(), 0.01);

pageSetup->set_Gutter(100.0);

// Ställ in egenskapen "RtlGutter" till "true" för att placera spåret på en mer lämplig position för höger‑till‑vänster‑text.
pageSetup->set_RtlGutter(true);

// Ställ in egenskapen "MultiplePages" till "MultiplePagesType.MirrorMargins" för att växla
// den vänstra/högra sidans marginalposition på varje sida.
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::MirrorMargins);

doc->Save(get_ArtifactsDir() + u"PageSetup.Gutter.docx");
```


Visar hur man konfigurerar ett dokument som kan skrivas ut som en bokvikt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Infoga text som sträcker sig över 16 sidor.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"My Booklet:");

for (int32_t i = 0; i < 15; i++)
{
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
    builder->Write(System::String::Format(u"Booklet face #{0}", i));
}

// Konfigurera den första sektionens egenskap "PageSetup" för att skriva ut dokumentet i form av en bokvikt.
// När vi skriver ut detta dokument på båda sidor kan vi ta sidorna för att stapla dem
// och vika dem alla ner i mitten på en gång. Dokumentets innehåll kommer att radas upp till en bokvikt.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_MultiplePages(Aspose::Words::Settings::MultiplePagesType::BookFoldPrinting);

// Vi kan endast ange antalet ark i multiplar av 4.
pageSetup->set_SheetsPerBooklet(4);

doc->Save(get_ArtifactsDir() + u"PageSetup.Booklet.docx");
```

## Se även

* Enum [MultiplePagesType](../../../aspose.words.settings/multiplepagestype/)
* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
