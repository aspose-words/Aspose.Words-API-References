---
title: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metod"
linktitle: "get_Password"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::OoxmlSaveOptions::get_Password metod. Hämtar/sätter ett lösenord för att kryptera dokumentet med ECMA376 Standard encryption algorithm i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.saving/ooxmlsaveoptions/get_password/
---
## OoxmlSaveOptions::get_Password method


Hämtar/anger ett lösenord för att kryptera dokumentet med ECMA376 Standard-krypteringsalgoritmen.

```cpp
System::String Aspose::Words::Saving::OoxmlSaveOptions::get_Password() const
```

## Anmärkningar


För att spara dokumentet utan kryptering bör denna egenskap vara **null** eller en tom sträng.

## Exempel



Visar hur man skapar ett lösenordskrypterat Office Open XML-dokument.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", saveOptions);

// Vi kommer inte att kunna öppna detta dokument med Microsoft Word eller
// Aspose.Words utan att ange rätt lösenord.
ASSERT_THROW(static_cast<std::function<void()>>([&doc]() -> void
{
    doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx");
})(), Aspose::Words::IncorrectPasswordException);

// Öppna det krypterade dokumentet genom att ange rätt lösenord i ett LoadOptions-objekt.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.Password.docx", System::MakeObject<Aspose::Words::Loading::LoadOptions>(u"MyPassword"));

ASSERT_EQ(u"Hello world!", doc->GetText().Trim());
```

## Se även

* Class [OoxmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
