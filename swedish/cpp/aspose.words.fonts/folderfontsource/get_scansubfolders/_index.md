---
title: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders method"
linktitle: "get_ScanSubfolders"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders metod. Bestämmer om underkatalogerna ska skannas i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.fonts/folderfontsource/get_scansubfolders/
---
## FolderFontSource::get_ScanSubfolders method


Bestämmer om underkataloger ska genomsökas eller inte.

```cpp
bool Aspose::Words::Fonts::FolderFontSource::get_ScanSubfolders() const
```


## Exempel



Visar hur man använder en lokal systemmapp som innehåller teckensnitt som en teckensnittskälla.
```cpp
// Skapa en teckensnittskälla från en mapp som innehåller teckensnittsfiler.
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false, 1);

auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({folderFontSource}));

ASSERT_EQ(get_FontsDir(), folderFontSource->get_FolderPath());
ASPOSE_ASSERT_EQ(false, folderFontSource->get_ScanSubfolders());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::FontsFolder, folderFontSource->get_Type());
ASSERT_EQ(1, folderFontSource->get_Priority());
```

## Se även

* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
