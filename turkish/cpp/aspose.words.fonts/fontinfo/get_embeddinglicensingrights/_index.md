---
title: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights yöntemi"
linktitle: "get_EmbeddingLicensingRights"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights yöntemi. C++'ta gömülü yazı tipi lisans haklarını alır."
type: docs
weight: 3500
url: /tr/cpp/aspose.words.fonts/fontinfo/get_embeddinglicensingrights/
---
## FontInfo::get_EmbeddingLicensingRights method


Gömülü yazı tipi lisans haklarını alır.

```cpp
System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> Aspose::Words::Fonts::FontInfo::get_EmbeddingLicensingRights()
```

## Açıklamalar


Değer, yazı tipi gömülü değilse null olabilir.

## Örnekler



Gömülü yazı tipleri için lisans hakları bilgilerini nasıl alacağınızı gösterir ([FontInfo](../)).
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

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [FontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
