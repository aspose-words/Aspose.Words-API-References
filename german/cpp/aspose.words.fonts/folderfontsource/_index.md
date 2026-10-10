---
title: "Aspose::Words::Fonts::FolderFontSource Klasse"
linktitle: "FolderFontSource"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FolderFontSource Klasse. Stellt den Ordner dar, der TrueType-Schriftdateien enthält. Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel in C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.fonts/folderfontsource/
---
## FolderFontSource class


Stellt den Ordner dar, der TrueType‑Schriftdateien enthält. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class FolderFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool) | Konstruktor. |
| [FolderFontSource](./folderfontsource/)(const System::String\&, bool, int32_t) | Konstruktor. |
| [get_FolderPath](./get_folderpath/)() const | Pfad zum Ordner. |
| [get_Priority](../fontsourcebase/get_priority/)() const | Gibt die Priorität der Schriftquellen zurück. |
| [get_ScanSubfolders](./get_scansubfolders/)() const | Bestimmt, ob Unterordner durchsucht werden sollen oder nicht. |
| [get_Type](./get_type/)() override | Gibt den Typ der Schriftquelle zurück. |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | Gibt eine Liste der über diese Quelle verfügbaren Schriften zurück. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Wird während der Verarbeitung der Schriftquelle aufgerufen, wenn ein Problem erkannt wird, das zu einem Verlust der Formatierungsgenauigkeit führen könnte. |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie ein lokaler Systemordner, der Schriften enthält, als Schriftquelle verwendet wird.
```cpp
// Erstellen Sie eine Schriftquelle aus einem Ordner, der Schriftdateien enthält.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Siehe auch

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
