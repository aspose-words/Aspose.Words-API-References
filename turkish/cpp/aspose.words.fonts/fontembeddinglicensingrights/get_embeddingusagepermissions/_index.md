---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions yöntemi"
linktitle: "get_EmbeddingUsagePermissions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions yöntemi. C++'ta kullanım izinleri."
type: docs
weight: 3000
url: /tr/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_embeddingusagepermissions/
---
## FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method


Kullanım izinleri.

```cpp
Aspose::Words::Fonts::FontEmbeddingUsagePermissions Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions() const
```


## Örnekler



Gömülü yazı tipleri için lisans hakları bilgilerini nasıl alacağınızı gösterir ([FontInfo](../../fontinfo/)).
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

* Enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
