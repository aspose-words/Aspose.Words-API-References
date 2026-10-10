---
title: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet metod"
linktitle: "get_PageSet"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet metod. Hämtar eller anger sidorna som ska renderas. Standard är alla sidor i dokumentet i C++."
type: docs
weight: 9000
url: /sv/cpp/aspose.words.saving/fixedpagesaveoptions/get_pageset/
---
## FixedPageSaveOptions::get_PageSet method


Hämtar eller anger sidorna som ska renderas. Standard är alla sidor i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Saving::PageSet> Aspose::Words::Saving::FixedPageSaveOptions::get_PageSet() const
```


## Exempel



Visar hur man extraherar sidor baserat på exakta sidindex.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Lägg till fem sidor i dokumentet.
for (int32_t i = 1; i < 6; i++)
{
    builder->Write(System::String(u"Page ") + i);
    builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
}

// Skapa ett "XpsSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod.
// för att ändra hur den metoden konverterar dokumentet till .XPS.
auto xpsOptions = System::MakeObject<Aspose::Words::Saving::XpsSaveOptions>();

// Använd egenskapen "PageSet" för att välja en uppsättning av dokumentets sidor som ska sparas till utdata‑XPS.
// I det här fallet kommer vi, via ett nollbaserat index, bara välja tre sidor: sida 1, sida 2 och sida 4.
xpsOptions->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(System::MakeArray<int32_t>({0, 1, 3})));

doc->Save(get_ArtifactsDir() + u"XpsSaveOptions.ExportExactPages.xps", xpsOptions);
```

## Se även

* Class [PageSet](../../pageset/)
* Class [FixedPageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
