---
title: "فئة Aspose::Words::Fonts::FontEmbeddingLicensingRights"
linktitle: "FontEmbeddingLicensingRights"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontEmbeddingLicensingRights. تمثل حقوق ترخيص التضمين للخط في C++."
type: docs
weight: 4500
url: /ar/cpp/aspose.words.fonts/fontembeddinglicensingrights/
---
## FontEmbeddingLicensingRights class


يمثل حقوق ترخيص تضمين الخط.

```cpp
class FontEmbeddingLicensingRights : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_BitmapEmbeddingOnly](./get_bitmapembeddingonly/)() const | يشير إلى القيد "تضمين البت ماب فقط". |
| [get_EmbeddingUsagePermissions](./get_embeddingusagepermissions/)() const | أذونات الاستخدام. |
| [get_NoSubsetting](./get_nosubsetting/)() const | يشير إلى القيد "بدون تقسيم". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يوضح كيفية الحصول على معلومات حقوق الترخيص للخطوط المضمنة ([FontInfo](../fontinfo/)).
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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
