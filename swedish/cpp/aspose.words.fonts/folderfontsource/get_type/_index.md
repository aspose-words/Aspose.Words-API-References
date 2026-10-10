---
title: "Aspose::Words::Fonts::FolderFontSource::get_Type metod"
linktitle: "get_Type"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::FolderFontSource::get_Type metod. Returnerar typ av teckensnittskällan i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words.fonts/folderfontsource/get_type/
---
## FolderFontSource::get_Type method


Returnerar typen av teckensnittskälla.

```cpp
Aspose::Words::Fonts::FontSourceType Aspose::Words::Fonts::FolderFontSource::get_Type() override
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

* Enum [FontSourceType](../../fontsourcetype/)
* Class [FolderFontSource](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
