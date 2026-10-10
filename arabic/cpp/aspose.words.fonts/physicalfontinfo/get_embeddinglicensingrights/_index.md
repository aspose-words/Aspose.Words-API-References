---
title: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights method"
linktitle: "get_EmbeddingLicensingRights"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights method. حقوق الترخيص للدمج للخط في C++."
type: docs
weight: 1500
url: /ar/cpp/aspose.words.fonts/physicalfontinfo/get_embeddinglicensingrights/
---
## PhysicalFontInfo::get_EmbeddingLicensingRights method


تضمين حقوق الترخيص للخط.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontEmbeddingLicensingRights> & Aspose::Words::Fonts::PhysicalFontInfo::get_EmbeddingLicensingRights() const
```


## أمثلة



يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المدمجة ([PhysicalFontInfo](../)).
```cpp
System::SharedPtr<Aspose::Words::Fonts::FontSettings> settings = Aspose::Words::Fonts::FontSettings::get_DefaultInstance();
System::SharedPtr<Aspose::Words::Fonts::FontSourceBase> source = settings->GetFontsSources()->idx_get(0);

// احصل على قائمة الخطوط المتاحة.
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

## انظر أيضًا

* Class [FontEmbeddingLicensingRights](../../fontembeddinglicensingrights/)
* Class [PhysicalFontInfo](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
