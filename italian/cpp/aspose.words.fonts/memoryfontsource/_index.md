---
title: "Aspose::Words::Fonts::MemoryFontSource class"
linktitle: "MemoryFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::MemoryFontSource class. Rappresenta il singolo file di carattere TrueType memorizzato in memoria. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 14000
url: /it/cpp/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class


Rappresenta il singolo file di carattere TrueType memorizzato in memoria. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class MemoryFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_CacheKey](./get_cachekey/)() const | La chiave di questa origine nella cache. |
| [get_FontData](./get_fontdata/)() const | Dati binari del carattere. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Restituisce la priorità della sorgente del font. |
| [get_Type](./get_type/)() override | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&) | Costruttore. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t) | Costruttore. |
| [MemoryFontSource](./memoryfontsource/)(const System::ArrayPtr\<uint8_t\>\&, int32_t, const System::String\&) | Costruttore. |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| static [Type](./type/)() |  |

## Esempi



Mostra come utilizzare un array di byte con i dati di un file di carattere come sorgente di caratteri.
```cpp
System::ArrayPtr<uint8_t> fontBytes = System::IO::File::ReadAllBytes(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf");
auto memoryFontSource = System::MakeObject<Aspose::Words::Fonts::MemoryFontSource>(fontBytes, 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({memoryFontSource}));

ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::MemoryFont, memoryFontSource->get_Type());
ASSERT_EQ(0, memoryFontSource->get_Priority());
```

## Vedi anche

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
