---
title: "فئة Aspose::Words::Fonts::TableSubstitutionRule"
linktitle: "TableSubstitutionRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::TableSubstitutionRule. قاعدة استبدال خطوط الجدول. لمعرفة المزيد، قم بزيارة مقالة الوثائق في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class


قاعدة استبدال الخط في الجدول. لمزيد من المعلومات، قم بزيارة مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class TableSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [AddSubstitutes](./addsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | يضيف أسماء خطوط بديلة للخط الأصلي المحدد. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | يحدد ما إذا كانت القاعدة مفعّلة أم لا. |
| [GetSubstitutes](./getsubstitutes/)(const System::String\&) | يرجع مصفوفة تحتوي على أسماء الخطوط البديلة للخط الأصلي المحدد. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Load](./load/)(const System::String\&) | يقوم بتحميل إعدادات استبدال الجدول من ملف XML. |
| [Load](./load/)(const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بتحميل إعدادات استبدال الجداول من تدفق XML. |
| [LoadAndroidSettings](./loadandroidsettings/)() | يقوم بتحميل إعدادات استبدال الجداول المحددة مسبقًا لمنصة Android. |
| [LoadLinuxSettings](./loadlinuxsettings/)() | يقوم بتحميل إعدادات استبدال الجداول المحددة مسبقًا لمنصة Linux. |
| [LoadWindowsSettings](./loadwindowssettings/)() | يقوم بتحميل إعدادات استبدال الجداول المحددة مسبقًا لمنصة Windows. |
| [Save](./save/)(const System::String\&) | يقوم بحفظ إعدادات استبدال الجداول الحالية إلى ملف. |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | يقوم بحفظ إعدادات استبدال الجداول الحالية إلى تدفق. |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | مُعيّن لـ [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| [SetSubstitutes](./setsubstitutes/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | تجاوز أسماء الخطوط البديلة لاسم الخط الأصلي المحدد. |
| static [Type](./type/)() |  |

## أمثلة



يعرض كيفية الوصول إلى جداول استبدال الخطوط لنظامي Windows و Linux.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// إنشاء قاعدة استبدال جدول جديدة وتحميل جدول استبدال خطوط Microsoft Windows الافتراضي.
System::SharedPtr<Aspose::Words::Fonts::TableSubstitutionRule> tableSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_TableSubstitution();
tableSubstitutionRule->LoadWindowsSettings();

// في نظام Windows، البديل الافتراضي لخط "Times New Roman CE" هو "Times New Roman".
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"Times New Roman"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// يمكننا حفظ الجدول على شكل مستند XML.
tableSubstitutionRule->Save(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Windows.xml");

// نظام Linux لديه جدول استبدال خاص به.
// هناك عدة خطوط بديلة لخط "Times New Roman CE".
// إذا كان البديل الأول، "FreeSerif" غير متوفر أيضًا،
// ستقوم هذه القاعدة بالتنقل عبر الآخرين في المصفوفة حتى تجد أحدًا متوفرًا.
tableSubstitutionRule->LoadLinuxSettings();
ASPOSE_ASSERT_EQ(System::MakeArray<System::String>({u"FreeSerif", u"Liberation Serif", u"DejaVu Serif"}), tableSubstitutionRule->GetSubstitutes(u"Times New Roman CE")->LINQ_ToArray());

// احفظ جدول استبدال Linux على شكل مستند XML باستخدام تدفق.
{
    auto fileStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"FontSettings.TableSubstitutionRule.Linux.xml", System::IO::FileMode::Create);
    tableSubstitutionRule->Save(fileStream);
}
```

## انظر أيضًا

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
