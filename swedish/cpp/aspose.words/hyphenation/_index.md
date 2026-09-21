---
title: "Aspose::Words::Hyphenation‑klass"
linktitle: "Avstavning"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Hyphenation‑klass. Tillhandahåller metoder för att arbeta med avstavningsordlistor. Dessa ordlistor anger var ord på ett specifikt språk kan avstavas. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 33000
url: /sv/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Tillhandahåller metoder för att arbeta med avstavningsordböcker. Dessa ordböcker anger var ord på ett specifikt språk kan avstavas. För att läsa mer, besök artikeln [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/) i dokumentationen.

```cpp
class Hyphenation
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| static [get_Callback](./get_callback/)() | Hämtar återuppringningsgränssnittet som används för att begära ordlistor när sidlayouten för dokumentet byggs. Detta möjliggör fördröjd inläsning av ordlistor, vilket kan vara användbart vid bearbetning av dokument på många språk. |
| static [get_WarningCallback](./get_warningcallback/)() | Kallas under inläsning av avstavningsmönster när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Returnerar **false** om det för det angivna språket inte finns någon registrerad ordlista eller om den registrerade är en Null‑ordlista, **true** annars. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Registrerar och laddar en avstavningsordlista för det angivna språket från en ström. Kastar ett undantag om ordlistan inte kan läsas eller har ett ogiltigt format. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Registrerar och laddar en avstavningsordlista för det angivna språket från en fil. Kastar ett undantag om ordlistan inte kan läsas eller har ett ogiltigt format. Denna metod kan också användas för att registrera en Null‑ordlista för att förhindra att [Callback](./get_callback/) anropas upprepade gånger för samma språk. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Ställer in återuppringningsgränssnittet som används för att begära ordböcker när sidlayouten för dokumentet byggs. Detta möjliggör fördröjd inläsning av ordböcker, vilket kan vara användbart vid bearbetning av dokument på många språk. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Kallas under inläsning av avstavningsmönster när ett problem upptäcks som kan leda till förlust av formateringsnoggrannhet. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Avregistrerar en avstavningsordbok för det angivna språket. Detta skiljer sig från att registrera en Null-ordbok. Att avregistrera en ordbok möjliggör återuppringning för det angivna språket. |
## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
