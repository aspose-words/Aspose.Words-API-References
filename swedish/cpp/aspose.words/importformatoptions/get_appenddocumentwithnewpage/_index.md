---
title: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metod"
linktitle: "get_AppendDocumentWithNewPage"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage metod. Hämtar eller anger ett booleskt värde som indikerar om den första importerade avsnittstypen ska ändras till NewPage tvångsmässigt när AppendDocument() anropas. Standardvärdet är true i C++."
type: docs
weight: 3500
url: /sv/cpp/aspose.words/importformatoptions/get_appenddocumentwithnewpage/
---
## ImportFormatOptions::get_AppendDocumentWithNewPage method


Hämtar eller anger ett booleskt värde som indikerar om den första importerade avsnittstypen ska ändras till [NewPage](../../sectionstart/) tvångsmässigt när [AppendDocument()](../) anropas. Standardvärdet är **true**.

```cpp
bool Aspose::Words::ImportFormatOptions::get_AppendDocumentWithNewPage() const
```


## Exempel



Visar hur man bevarar originalavsnittstypen.
```cpp
auto dstDoc = System::MakeObject<Aspose::Words::Document>();
auto srcDoc = System::MakeObject<Aspose::Words::Document>();

srcDoc->get_FirstSection()->get_PageSetup()->set_SectionStart(Aspose::Words::SectionStart::Continuous);

auto options = System::MakeObject<Aspose::Words::ImportFormatOptions>();
options->set_AppendDocumentWithNewPage(false);
dstDoc->AppendDocument(srcDoc, Aspose::Words::ImportFormatMode::KeepSourceFormatting, options);

ASSERT_EQ(Aspose::Words::SectionStart::Continuous, dstDoc->get_Sections()->idx_get(1)->get_PageSetup()->get_SectionStart());
```

## Se även

* Class [ImportFormatOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
