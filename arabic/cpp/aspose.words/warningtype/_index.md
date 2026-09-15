---
title: "تعداد Aspose::Words::WarningType"
linktitle: "WarningType"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::WarningType. يحدد نوع التحذير الذي تصدره Aspose.Words أثناء تحميل المستند أو حفظه في C++."
type: docs
weight: 129000
url: /ar/cpp/aspose.words/warningtype/
---
## WarningType enum


يحدد نوع التحذير الذي تصدره Aspose.Words أثناء تحميل المستند أو حفظه.

```cpp
enum class WarningType
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| DataLossCategory | 255 | قد يكون بعض النص/الحرف/الصورة أو بيانات أخرى مفقودة إما من شجرة المستند بعد التحميل، أو من المستند المُنشأ بعد الحفظ. |
| DataLoss | 1 | فقدان بيانات عام، بدون رمز محدد. |
| MajorFormattingLossCategory | 65280 | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا بشكل كبير مقارنة بالمستند الأصلي. |
| MajorFormattingLoss | 256 | فقدان تنسيق رئيسي عام، بدون رمز محدد. |
| MinorFormattingLossCategory | 16711680 | قد يبدو المستند الناتج أو موقع معين فيه مختلفًا إلى حد ما مقارنة بالمستند الأصلي. |
| MinorFormattingLoss | 65536 | فقدان تنسيق طفيف عام، لا يوجد رمز محدد. |
| FontSubstitution | 131072 | [Font](../font/) تم استبداله. |
| FontEmbedding | 262144 | فقدان معلومات الخط المدمج أثناء حفظ المستند. |
| UnexpectedContentCategory | 251658240 | بعض المحتوى في المستند الأصلي لم يتم التعرف عليه (أي غير مدعوم)، قد يسبب ذلك مشاكل أو قد لا يسبب، وقد يؤدي إلى فقدان البيانات أو التنسيق. |
| UnexpectedContent | 16777216 | محتوى غير متوقع عام، لا يوجد رمز محدد. |
| تلميح | 268435456 | ينصح بوجود مشكلة محتملة أو يقترح تحسينًا. |


## أمثلة



يظهر كيفية ضبط الخاصية للعثور على أقرب تطابق لخط مفقود من مصادر الخطوط المتاحة.
```cpp
// افتح مستندًا يحتوي على نص منسق بخط غير موجود في أي من مصادر الخطوط لدينا.
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// عيّن رد نداء لمعالجة تحذيرات استبدال الخطوط.
auto warningCollector = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warningCollector);

// حدد اسم خط افتراضي وقم بتمكين استبدال الخط.
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);

// يجب استخدام مقاييس الخط الأصلي بعد استبدال الخط.
doc->get_LayoutOptions()->set_KeepOriginalFontMetrics(true);

// سوف نحصل على تحذير استبدال الخط إذا حفظنا مستندًا بخط مفقود.
doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.EnableFontSubstitution.pdf");

for (auto&& info : warningCollector)
{
    if (info->get_WarningType() == Aspose::Words::WarningType::FontSubstitution)
    {
        std::cout << info->get_Description() << std::endl;
    }
}
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
