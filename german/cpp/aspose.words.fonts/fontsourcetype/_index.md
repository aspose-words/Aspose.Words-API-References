---
title: "Aspose::Words::Fonts::FontSourceType enum"
linktitle: "FontSourceType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FontSourceType enum. Gibt den Typ der Schriftquellen in C++ an."
type: docs
weight: 23000
url: /de/cpp/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enum


Gibt den Typ der Schriftquelle an.

```cpp
enum class FontSourceType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FontFile | 0 | Ein [FileFontSource](../filefontsource/)-Objekt, das eine einzelne Schriftdatei darstellt. |
| FontsFolder | 1 | Ein [FolderFontSource](../folderfontsource/) Objekt, das einen Ordner mit Schriftdateien darstellt. |
| MemoryFont | 2 | Ein [MemoryFontSource](../memoryfontsource/) Objekt, das eine einzelne Schriftart im Speicher darstellt. |
| SystemFonts | 3 | Ein [SystemFontSource](../systemfontsource/) Objekt, das alle im System installierten Schriftarten darstellt. |
| FontStream | 4 | Ein [StreamFontSource](../streamfontsource/) Objekt, das einen Stream mit Schriftartdaten darstellt. |


## Beispiele



Zeigt, wie man eine Schriftdatei im lokalen Dateisystem als Schriftquelle verwendet.
```cpp
auto fileFontSource = System::MakeObject<Aspose::Words::Fonts::FileFontSource>(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", 0);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({fileFontSource}));

ASSERT_EQ(get_MyDir() + u"Alte DIN 1451 Mittelschrift.ttf", fileFontSource->get_FilePath());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontFile, fileFontSource->get_Type());
ASSERT_EQ(0, fileFontSource->get_Priority());
```

## Siehe auch

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
