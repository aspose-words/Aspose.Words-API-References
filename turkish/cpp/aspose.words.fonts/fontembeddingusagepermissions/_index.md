---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. C++'de font gömme kullanım izinlerini temsil eder."
type: docs
weight: 20500
url: /tr/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


Yazı tipi gömme kullanım izinlerini temsil eder.

```cpp
enum class FontEmbeddingUsagePermissions
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Installable | 0 | Font gömülebilir ve uzak sistemlerde kullanım için kalıcı olarak kurulabilir ya da diğer kullanıcılar tarafından kullanılabilir. |
| RestrictedLicense | 1 | Font, yasal sahibinden açık izin alınmadan hiçbir şekilde değiştirilemez, gömülemez veya değiş tokuş edilemez. |
| PrintAndPreview | 2 | Font gömülebilir ve belgeyi görüntüleme veya yazdırma amaçlarıyla diğer sistemlerde geçici olarak yüklenebilir. |
| Editable | 3 | Font gömülebilir ve diğer sistemlerde geçici olarak yüklenebilir. |


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
