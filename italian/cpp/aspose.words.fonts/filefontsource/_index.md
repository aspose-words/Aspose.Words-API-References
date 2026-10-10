---
title: "Aspose::Words::Fonts::FileFontSource class"
linktitle: "FileFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FileFontSource class. Rappresenta il singolo file TrueType memorizzato nel file system. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words.fonts/filefontsource/
---
## FileFontSource class


Rappresenta il singolo file di carattere TrueType memorizzato nel file system. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FileFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FileFontSource](./filefontsource/)(const System::String\&) | Costruttore. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t) | Costruttore. |
| [FileFontSource](./filefontsource/)(const System::String\&, int32_t, const System::String\&) | Costruttore. |
| [get_CacheKey](./get_cachekey/)() const | La chiave di questa origine nella cache. |
| [get_FilePath](./get_filepath/)() const | Percorso del file del font. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Restituisce la priorità della sorgente del font. |
| [get_Type](./get_type/)() override | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| static [Type](./type/)() |  |

## Esempi



Mostra come utilizzare un file di font nel file system locale come origine del font.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Vedi anche

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
