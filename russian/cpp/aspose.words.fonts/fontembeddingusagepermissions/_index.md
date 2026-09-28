---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. Представляет разрешения на встраивание шрифтов в C++."
type: docs
weight: 20500
url: /ru/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Представляет разрешения на использование встроенных шрифтов.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| Installable | 0 | Шрифт может быть встроен и может быть постоянно установлен для использования на удалённых системах или другими пользователями. |
| RestrictedLicense | 1 | Шрифт не должен изменяться, встраиваться или передаваться каким-либо образом без предварительного получения явного разрешения от законного владельца. |
| PrintAndPreview | 2 | Шрифт может быть встроен и может временно загружаться на другие системы для просмотра или печати документа. |
| Editable | 3 | Шрифт может быть встроен и может временно загружаться на другие системы. |


## Примеры



Показывает, как получить информацию о правах лицензии для встроенных шрифтов ([FontInfo](../fontinfo/)).
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
