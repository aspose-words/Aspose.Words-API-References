---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights класс"
linktitle: "FontEmbeddingLicensingRights"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights класс. Представляет права лицензии на встраивание шрифта в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Представляет права лицензии на встраивание шрифта.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | Указывает ограничение «Только встраивание растрового изображения». |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Разрешения на использование. |
| [get_NoSubsetting](./get_nosubsetting/)() const | Указывает ограничение «Без подмножества». |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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
