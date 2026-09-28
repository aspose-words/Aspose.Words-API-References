---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights метод"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights метод. Права лицензирования встраивания шрифта в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.fonts/physicalfontinfo/get_embeddinglicensingrights/
---
## PhysicalFontInfo::get_EmbeddingLicensingRights method


Встраивание прав лицензирования для шрифта.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> & Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights() const
```


## Примеры



Показывает, как получить информацию о правах лицензии для встроенных шрифтов ([PhysicalFontInfo](../)).
```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> settings = Aspose::Words::Fonts::FontSettings::get_DefaultInstance();
System::SharedPtr<Aspose::Words::Fonts::FontSourceBase> source = settings->GetFontsSources()->idx_get(0);

// Получите список доступных шрифтов.
System::SharedPtr<System::Collections::Generic::IList<System::SharedPtr<Aspose::Words::Fonts::PhysicalFontInfo>>> fontInfos = source->GetAvailableFonts();
for (auto&& fontInfo : System::IterateOver(fontInfos))
{
    if (fontInfo->get_EmbeddingLicensingRights() != nullptr)
    {
        std::cout << System::EnumGetName(fontInfo->get_EmbeddingLicensingRights()->get_EmbeddingUsagePermissions()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_BitmapEmbeddingOnly()) << std::endl;
        std::cout << System::Convert::ToString(fontInfo->get_EmbeddingLicensingRights()->get_NoSubsetting()) << std::endl;
    }
}
```

## См. также

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
