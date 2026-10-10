---
title: "Aspose::Words::Fonts::FolderFontSource::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FolderFontSource::get_Type Methode. Gibt den Typ der Schriftquellen in C++ zurück."
type: docs
weight: 5000
url: /de/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


Gibt den Typ der Schriftquelle zurück.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
```


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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
