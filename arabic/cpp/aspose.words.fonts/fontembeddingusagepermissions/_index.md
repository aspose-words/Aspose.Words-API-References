---
title: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum"
linktitle: "FontEmbeddingUsagePermissions"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontEmbeddingUsagePermissions enum. يمثل أذونات استخدام تضمين الخط في C++."
type: docs
weight: 20500
url: /ar/cpp/aspose.words.fonts/fontembeddingusagepermissions/
---
## FontEmbeddingUsagePermissions enum


يمثل أذونات استخدام تضمين الخط.

```cpp
enum class FontEmbeddingUsagePermissions
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| Installable | 0 | يمكن تضمين الخط، وقد يتم تثبيته بشكل دائم للاستخدام على أنظمة بعيدة، أو للاستخدام من قبل مستخدمين آخرين. |
| RestrictedLicense | 1 | يجب عدم تعديل الخط أو تضمينه أو تبادله بأي طريقة دون الحصول أولاً على إذن صريح من المالك القانوني. |
| PrintAndPreview | 2 | يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى لأغراض عرض أو طباعة المستند. |
| Editable | 3 | يمكن تضمين الخط، وقد يتم تحميله مؤقتًا على أنظمة أخرى. |


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
