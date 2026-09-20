---
title: "Метод Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions"
linktitle: "get_EmbeddingUsagePermissions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions. Права использования в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_embeddingusagepermissions/
---
## FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method


Разрешения на использование.

```cpp
Aspose::Words::Fonts::FontEmbeddingUsagePermissions Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions() const
```


## Примеры



Показывает, как получить информацию о правах лицензии для внедрённых шрифтов ([FontInfo](../../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Получить список шрифтов документа.
System::SharedPtr<Aspose::Words::Fonts::FontInfoCollection> fontInfos = doc->get_FontInfos();
for (auto&& fontInfo : fontInfos)
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

* Enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
