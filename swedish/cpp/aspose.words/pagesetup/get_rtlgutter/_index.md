---
title: "Aspose::Words::PageSetup::get_RtlGutter metod"
linktitle: "get_RtlGutter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PageSetup::get_RtlGutter metod. Hämtar eller anger om Microsoft Word använder spalter för sektionen baserat på ett språk som skrivs från höger till vänster eller från vänster till höger i C++."
type: docs
weight: 40000
url: /sv/cpp/aspose.words/pagesetup/get_rtlgutter/
---
## PageSetup::get_RtlGutter method


Hämtar eller anger om Microsoft Word använder marginaler för avsnittet baserat på ett språk som skrivs från höger till vänster eller från vänster till höger.

```cpp
bool Aspose::Words::PageSetup::get_RtlGutter()
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

## Se även

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
