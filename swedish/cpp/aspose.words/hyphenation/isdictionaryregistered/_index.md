---
title: "Aspose::Words::Hyphenation::IsDictionaryRegistered metod"
linktitle: "IsDictionaryRegistered"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Hyphenation::IsDictionaryRegistered metod. Returnerar false om det för det angivna språket inte finns någon registrerad ordbok eller om den registrerade är en Null‑ordbok, true annars i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation::IsDictionaryRegistered method


Returnerar **false** om det för det angivna språket inte finns någon registrerad ordlista eller om den registrerade är en Null‑ordlista, **true** annars.

```cpp
static bool Aspose::Words::Hyphenation::IsDictionaryRegistered(const System::String &language)
```


## Exempel



Visar hur man registrerar en avstavningsordbok.
```cpp
// En avstavningsordbok innehåller en lista med strängar som definierar avstavningsregler för ordbokens språk.
// När ett dokument innehåller textrader där ett ord kan delas upp och fortsättas på nästa rad,
// kommer avstavning att söka igenom ordbokens lista med strängar efter delsträngar av det ordet.
// Om ordboken innehåller en delsträng kommer avstavning att dela ordet över två rader
// av delsträngen och lägg till ett bindestreck i den första halvan.
// Registrera en ordboksfil från det lokala filsystemet till "de-CH"-lokalen.
Aspose::Words::Hyphenation::RegisterDictionary(u"de-CH", get_MyDir() + u"hyph_de_CH.dic");

ASSERT_TRUE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

// Öppna ett dokument som innehåller text med en lokal som matchar vår ordbok,
// och spara det i ett fast-sidigt sparformat. Texten i det dokumentet kommer att bindestreckas.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->LINQ_OfType<System::SharedPtr<Aspose::Words::Run> >()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::Run>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Run> r)>>([](System::SharedPtr<Aspose::Words::Run> r) -> bool
{
    return r->get_Font()->get_LocaleId() == System::MakeObject<System::Globalization::CultureInfo>(u"de-CH")->get_LCID();
}))));

doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Registered.pdf");

// Läs in dokumentet igen efter att ha avregistrerat ordboken,
// och spara det till en annan PDF, som inte kommer att ha bindestreckad text.
Aspose::Words::Hyphenation::UnregisterDictionary(u"de-CH");

ASSERT_FALSE(Aspose::Words::Hyphenation::IsDictionaryRegistered(u"de-CH"));

doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"German text.docx");
doc->Save(get_ArtifactsDir() + u"Hyphenation.Dictionary.Unregistered.pdf");
```

## Se även

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
