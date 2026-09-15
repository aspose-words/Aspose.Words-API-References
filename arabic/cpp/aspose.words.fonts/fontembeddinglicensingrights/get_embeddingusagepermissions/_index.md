---
title: "طريقة Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions"
linktitle: "get_EmbeddingUsagePermissions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions. أذونات الاستخدام في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_embeddingusagepermissions/
---
## FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions method


أذونات الاستخدام.

```cpp
Aspose::Words::Fonts::FontEmbeddingUsagePermissions Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_EmbeddingUsagePermissions() const
```


## أمثلة



يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المدمجة ([FontInfo](../../fontinfo/)).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Embedded font rights.docx");

// احصل على قائمة خطوط المستند.
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

## انظر أيضًا

* Enum [FontEmbeddingUsagePermissions](../../fontembeddingusagepermissions/)
* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
