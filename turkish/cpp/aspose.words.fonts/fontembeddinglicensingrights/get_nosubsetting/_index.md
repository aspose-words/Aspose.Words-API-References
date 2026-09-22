---
title: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting yöntemi"
linktitle: "get_NoSubsetting"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting yöntemi. C++'ta \"No subsetting\" kısıtlamasını gösterir."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_nosubsetting/
---
## FontEmbeddingLicensingRights::get_NoSubsetting method


"No subsetting" kısıtlamasını gösterir.

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_NoSubsetting() const
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
