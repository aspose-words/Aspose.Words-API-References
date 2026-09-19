---
title: "Aspose::Words::Fonts::FolderFontSource classe"
linktitle: "FolderFontSource"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fonts::FolderFontSource classe. Rappresenta la cartella che contiene file di font TrueType. Per saperne di più, visita l'articolo della documentazione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Rappresenta la cartella che contiene i file di caratteri TrueType. Per saperne di più, visita l'articolo di documentazione [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Costruttore. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Costruttore. |
| [get_FolderPath](./get_folderpath/)() const | Percorso della cartella. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Restituisce la priorità della sorgente del font. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Determina se eseguire o meno la scansione delle sottocartelle. |
| [get_Type](./get_type/)() override | Restituisce il tipo della sorgente del font. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Restituisce l'elenco dei font disponibili tramite questa sorgente. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Chiamato durante l'elaborazione della sorgente del font quando viene rilevato un problema che potrebbe causare una perdita di fedeltà della formattazione. |
| static [Type](./type/)() |  |

## Esempi



Mostra come utilizzare una cartella di sistema locale che contiene font come sorgente di font.
```cpp
// Crea una sorgente di font da una cartella che contiene file di font.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Vedi anche

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
