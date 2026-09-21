---
title: "Aspose::Words::Loading::LoadOptions::get_Encoding metod"
linktitle: "get_Encoding"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::LoadOptions::get_Encoding metod. Hämtar eller anger den kodning som kommer att användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara null. Standard är null i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.loading/loadoptions/get_encoding/
---
## LoadOptions::get_Encoding method


Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara **null**. Standardvärdet är **null**.

```cpp
System::SharedPtr<System::Text::Encoding> Aspose::Words::Loading::LoadOptions::get_Encoding() const
```

## Anmärkningar


Denna egenskap används endast vid inläsning av HTML-, TXT- eller CHM-dokument.

Om kodning inte är specificerad i dokumentet och denna egenskap är **null**, kommer systemet att försöka automatiskt upptäcka kodningen.

## Exempel



Visar hur man anger den kodning som ska användas för att öppna ett dokument.
```cpp
auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Encoding(System::Text::Encoding::get_ASCII());

// Läs in dokumentet samtidigt som du skickar LoadOptions-objektet, verifiera sedan dokumentets innehåll.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"English text.txt", loadOptions);

ASSERT_TRUE(doc->ToString(Aspose::Words::SaveFormat::Text).Contains(u"This is a sample text in English."));
```

## Se även

* Class [LoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
