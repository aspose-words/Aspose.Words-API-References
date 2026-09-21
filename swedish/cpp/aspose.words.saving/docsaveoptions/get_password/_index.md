---
title: "Aspose::Words::Saving::DocSaveOptions::get_Password metod"
linktitle: "get_Password"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::DocSaveOptions::get_Password metod. Hämtar/sätter ett lösenord för att kryptera dokumentet med RC4-krypteringsmetod i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/docsaveoptions/get_password/
---
## DocSaveOptions::get_Password method


Hämtar/anger ett lösenord för att kryptera dokumentet med RC4‑krypteringsmetoden.

```cpp
System::String Aspose::Words::Saving::DocSaveOptions::get_Password() const
```

## Anmärkningar


För att spara dokumentet utan kryptering bör denna egenskap vara **null** eller en tom sträng.

## Exempel



Visar hur man ställer in sparalternativ för äldre Microsoft Word-format.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto options = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>(Aspose::Words::SaveFormat::Doc);

// Ställ in ett lösenord som skyddar inläsning av dokumentet i Microsoft Word eller Aspose.Words.
// Observera att detta inte krypterar dokumentets innehåll på något sätt.
options->set_Password(u"MyPassword");

// Om dokumentet innehåller ett routningsblad kan vi bevara det vid sparning genom att sätta denna flagga till true.
options->set_SaveRoutingSlip(true);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", options);

// För att kunna ladda dokumentet,
// måste vi tillämpa lösenordet som vi specificerade i DocSaveOptions-objektet i ett LoadOptions-objekt.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc");
})(), Aspose::Words::IncorrectPasswordException);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.SaveAsDoc.doc", loadOptions);

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Class [DocSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
