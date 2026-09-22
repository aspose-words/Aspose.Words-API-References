---
title: "طريقة Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly"
linktitle: "get_BitmapEmbeddingOnly"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly. تشير إلى قيود \"Bitmap embedding only\" في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/fontembeddinglicensingrights/get_bitmapembeddingonly/
---
## FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly method


يشير إلى القيد "تضمين البت ماب فقط".

```cpp
bool Aspose::Words::Fonts::FontEmbeddingLicensingRights::get_BitmapEmbeddingOnly() const
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

* Class [FontEmbeddingLicensingRights](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
