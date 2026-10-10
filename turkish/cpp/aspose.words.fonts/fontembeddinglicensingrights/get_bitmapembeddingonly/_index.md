---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly yöntemi"
linktitle: "get_BitmapEmbeddingOnly"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly yöntemi. C++'ta \"Bitmap embedding only\" kısıtlamasını gösterir."
type: docs
weight: 2000
url: /tr/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_bitmapembeddingonly/
---
## FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method


"Bitmap embedding only" kısıtlamasını gösterir.

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly() const
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

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
