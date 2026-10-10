---
title: "Aspose::Words::Fonts::DefaultFontSubstitutionRule فئة"
linktitle: "DefaultFontSubstitutionRule"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::Fonts::DefaultFontSubstitutionRule. قاعدة استبدال الخط الافتراضي. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.fonts/defaultfontsubstitutionrule/
---
## DefaultFontSubstitutionRule class


قاعدة استبدال الخط الافتراضية. لمعرفة المزيد، زر مقالة الوثائق [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/).

```cpp
class DefaultFontSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_DefaultFontName](./get_defaultfontname/)() | يحصل على أو يضبط اسم الخط الافتراضي. |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | يحدد ما إذا كانت القاعدة مفعّلة أم لا. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_DefaultFontName](./set_defaultfontname/)(const System::String\&) | مُعيّن لـ [Aspose::Words::Fonts::DefaultFontSubstitutionRule::get_DefaultFontName](./get_defaultfontname/). |
| virtual [set_Enabled](../fontsubstitutionrule/set_enabled/)(bool) | مُعيّن لـ [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](../fontsubstitutionrule/get_enabled/). |
| static [Type](./type/)() |  |

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
