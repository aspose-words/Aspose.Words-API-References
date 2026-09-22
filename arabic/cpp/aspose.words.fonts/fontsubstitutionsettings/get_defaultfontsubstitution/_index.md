---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution طريقة"
linktitle: "get_DefaultFontSubstitution"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution طريقة. الإعدادات المتعلقة بقاعدة استبدال الخط الافتراضي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.fonts/fontsubstitutionsettings/get_defaultfontsubstitution/
---
## FontSubstitutionSettings::get_DefaultFontSubstitution method


[Settings](../../../aspose.words.settings/) related to default font substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_DefaultFontSubstitution() const
```


## أمثلة



يعرض كيفية ضبط قاعدة استبدال الخط الافتراضي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
doc->set_FontSettings(fontSettings);

// احصل على قاعدة الاستبدال الافتراضية داخل FontSettings.
// ستستبدل هذه القاعدة جميع الخطوط المفقودة بـ "Times New Roman".
System::SharedPtr<Aspose::Words::Fonts::DefaultFontSubstitutionRule> defaultFontSubstitutionRule = fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution();
ASSERT_TRUE(defaultFontSubstitutionRule->get_Enabled());
ASSERT_EQ(u"Times New Roman", defaultFontSubstitutionRule->get_DefaultFontName());

// عيّن بديل الخط الافتراضي إلى "Courier New".
defaultFontSubstitutionRule->set_DefaultFontName(u"Courier New");

// باستخدام مُنشئ المستند، أضف بعض النص بخط لا نمتلكه لنرى حدوث الاستبدال،
// ثم قم بتصدير النتيجة إلى ملف PDF.
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Missing Font");
builder->Writeln(u"Line written in a missing font, which will be substituted with Courier New.");

doc->Save(get_ArtifactsDir() + u"FontSettings.DefaultFontSubstitutionRule.pdf");
```

## انظر أيضًا

* Class [DefaultFontSubstitutionRule](../../defaultfontsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
