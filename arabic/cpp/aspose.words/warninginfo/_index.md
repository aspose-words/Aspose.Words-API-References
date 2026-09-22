---
title: "Aspose::Words::WarningInfo فئة"
linktitle: "WarningInfo"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::WarningInfo. يحتوي على معلومات حول تحذير أصدرته Aspose.Words أثناء تحميل المستند أو حفظه. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 74000
url: /ar/cpp/aspose.words/warninginfo/
---
## WarningInfo class


يحتوي على معلومات حول تحذير أصدرته Aspose.Words أثناء تحميل أو حفظ المستند. لمعرفة المزيد، زر مقالة الوثائق [Programming with Documents](https://docs.aspose.com/words/cpp/programming-with-documents/).

```cpp
class WarningInfo : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Description](./get_description/)() const | يعيد وصف التحذير. |
| [get_Source](./get_source/)() const | يعيد مصدر التحذير. |
| [get_WarningType](./get_warningtype/)() const | يعيد نوع التحذير. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## ملاحظات


أنت لا تنشئ مثيلات من هذه الفئة. يتم إنشاء كائنات هذه الفئة وتمريرها بواسطة Aspose.Words إلى طريقة [Warning()](../iwarningcallback/warning/).

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
