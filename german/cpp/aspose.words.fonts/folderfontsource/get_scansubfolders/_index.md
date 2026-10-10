---
title: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders Methode"
linktitle: "get_ScanSubfolders"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders Methode. Bestimmt, ob Unterordner in C++ gescannt werden sollen oder nicht."
type: docs
weight: 4000
url: /de/cpp/aspose.words.fonts/folderfontsource/get_scansubfolders/
---
## FolderFontSource::get_ScanSubfolders method


Bestimmt, ob Unterordner durchsucht werden sollen oder nicht.

```cpp
bool Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders() const
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

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
