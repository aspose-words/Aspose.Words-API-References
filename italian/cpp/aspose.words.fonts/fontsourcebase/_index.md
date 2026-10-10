---
title: "Aspose::Words::Fonts::FontSourceBase class"
linktitle: "FontSourceBase"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FontSourceBase class. Questa è una classe base astratta per le classi che consentono all'utente di specificare varie sorgenti di caratteri. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 11000
url: /it/cpp/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class


Questa è una classe base astratta per le classi che consentono all'utente di specificare varie origini dei caratteri. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FontSourceBase : public Aspose::Fonts::IFontSource
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Priority](./get_priority/)() const | Restituisce la priorità della sorgente del font. |
| virtual [get_Type](./get_type/)() | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](./get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](./getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
