---
title: "فئة Aspose::Words::Fonts::FontInfoSubstitutionRule"
linktitle: "FontInfoSubstitutionRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::FontInfoSubstitutionRule. قاعدة استبدال معلومات الخط. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.fonts/fontinfosubstitutionrule/
---
## FontInfoSubstitutionRule class


[Font](../../aspose.words/font/) info substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontInfoSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | يحدد ما إذا كانت القاعدة مفعّلة أم لا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | مُعيّن لـ [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
