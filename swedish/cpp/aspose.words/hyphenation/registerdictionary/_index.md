---
title: "Aspose::Words::Hyphenation::RegisterDictionary method"
linktitle: "RegisterDictionary"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Hyphenation::RegisterDictionary method. Registrerar och laddar en bindestrecksordbok för det angivna språket från en ström. Kastar ett undantag om ordboken inte kan läsas eller har ett ogiltigt format i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words/hyphenation/registerdictionary/
---
## Hyphenation::RegisterDictionary(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Registrerar och laddar en avstavningsordlista för det angivna språket från en ström. Kastar ett undantag om ordlistan inte kan läsas eller har ett ogiltigt format.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| språk | const System::String\& | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "culture name" och RFC 4646 för detaljer. |
| ström | const System::SharedPtr\<System::IO::Stream\>\& | En ström för ordboksfilen i OpenOffice-format. |

## Se även

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Hyphenation::RegisterDictionary(const System::String\&, const System::String\&) method


Registrerar och laddar en bindestrecksordbok för det angivna språket från fil. Kastar ett undantag om ordboken inte kan läsas eller har ett ogiltigt format. Denna metod kan också användas för att registrera en Null-ordbok för att förhindra att [Callback](../get_callback/) anropas upprepade gånger för samma språk.

```cpp
static void Aspose::Words::Hyphenation::RegisterDictionary(const System::String &language, const System::String &fileName)
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| språk | const System::String\& | Ett språknamn, t.ex. "en-US". Se .NET-dokumentationen för "culture name" och RFC 4646 för detaljer. |
| fileName | const System::String\& | En sökväg till ordboksfilen i Open Office-format. Om den här parametern är **null** eller tom sträng så registreras en Null-ordbok och återanrop anropas inte längre för detta språk. För att aktivera återanrop igen, använd [UnregisterDictionary()](../) metoden. |

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
## Hyphenation::RegisterDictionary(System::String, std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::Hyphenation::RegisterDictionary(System::String language, std::basic_istream<CharType, Traits> &stream)
```

## Se även

* Class [Hyphenation](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
