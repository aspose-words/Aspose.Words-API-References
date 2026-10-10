---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights class"
linktitle: "FontEmbeddingLicensingRights"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights sınıfı. C++'ta yazı tipi için gömme lisans haklarını temsil eder."
type: docs
weight: 4500
url: /tr/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


Yazı tipi için gömme lisans haklarını temsil eder.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | "Bitmap embedding only" kısıtlamasını gösterir. |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | Kullanım izinleri. |
| [get_NoSubsetting](./get_nosubsetting/)() const | "No subsetting" kısıtlamasını gösterir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Gömülü fontlar için lisans hakları bilgilerini nasıl alacağınızı gösterir ([FontInfo](../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// Belge fontlarının listesini al.
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
