---
title: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings طريقة"
linktitle: "LoadWindowsSettings"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings طريقة. يحمل إعدادات استبدال الجداول المعرفة مسبقًا لمنصة Windows في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule::LoadWindowsSettings method


يقوم بتحميل إعدادات استبدال الجداول المحددة مسبقًا لمنصة Windows.

```cpp
void Aspose::Words::Fonts::TableSubstitutionRule::LoadWindowsSettings()
```


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

* Class [TableSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
