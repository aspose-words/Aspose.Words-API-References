---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights method"
linktitle: "get_EmbeddingLicensingRights"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights‑metoden. Inbäddningslicensrättigheter för teckensnittet i C++."
type: docs
weight: 1500
url: /sv/cpp/aspose.words.fonts/physicalfontinfo/get_embeddinglicensingrights/
---
## PhysicalFontInfo::get_EmbeddingLicensingRights method


Inbäddning av licensrättigheter för teckensnittet.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> & Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights() const
```


## Exempel



Visar hur man får information om licensrättigheter för inbäddade teckensnitt ([PhysicalFontInfo](../)).
```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> settings = Aspose::Words::Fonts::FontSettings::get_DefaultInstance();
System::SharedPtr<Aspose::Words::Fonts::FontSourceBase> source = settings->GetFontsSources()->idx_get(0);

// Hämta listan över tillgängliga teckensnitt.
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

## Se även

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
