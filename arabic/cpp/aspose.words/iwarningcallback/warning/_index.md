---
title: "طريقة Aspose::Words::IWarningCallback::Warning"
linktitle: "تحذير"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::IWarningCallback::Warning. تقوم Aspose.Words باستدعاء هذه الطريقة عندما تواجه مشكلة أثناء تحميل أو حفظ المستند قد تؤدي إلى فقدان التنسيق أو دقة البيانات في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/iwarningcallback/warning/
---
## IWarningCallback::Warning method


Aspose.Words يستدعي هذه الطريقة عندما يصادف مشكلة أثناء تحميل أو حفظ المستند قد تؤدي إلى فقدان التنسيق أو دقة البيانات.

```cpp
virtual void Aspose::Words::IWarningCallback::Warning(System::SharedPtr<Aspose::Words::WarningInfo> info)=0
```


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

* Class [WarningInfo](../../warninginfo/)
* Interface [IWarningCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
