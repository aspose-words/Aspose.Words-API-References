---
title: "Aspose::Words::Themes::ThemeColors::get_Dark2 طريقة"
linktitle: "get_Dark2"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Themes::ThemeColors::get_Dark2 طريقة. تحدد اللون Dark 2 في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words.themes/themecolors/get_dark2/
---
## ThemeColors::get_Dark2 method


يحدد اللون Dark 2.

```cpp
System::Drawing::Color Aspose::Words::Themes::ThemeColors::get_Dark2()
```


## أمثلة



يعرض كيفية تعيين ألوان وخطوط مخصصة للثيمات.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// كائن \"Theme\" يمنحنا الوصول إلى ثيم المستند، وهو مصدر الخطوط والألوان الافتراضية.
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// بعض الأنماط، مثل \"Heading 1\" و \"Subtitle\"، ستورث هذه الخطوط.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// قد تحتوي اللغات الأخرى أيضًا على خطوط مخصصة في هذا الثيم.
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// خاصية \"Colors\" تحتوي على لوحة الألوان من Microsoft Word،
// التي تظهر عند تغيير التظليل أو لون الخط.
// طبق ألوانًا مخصصة على لوحة الألوان حتى نتمكن من الوصول إليها بسهولة في Microsoft Word
// عندما نقوم، على سبيل المثال، بتغيير لون الخط عبر \"Home\" -> \"Font\" -> \"Font Color\",
// أو إدراج شكل، ثم تعيين لون له عبر \"Shape Format\" -> \"Shape Styles\".
System::SharedPtr<Aspose::Words::Themes::ThemeColors> colors = theme->get_Colors();
colors->set_Dark1(System::Drawing::Color::get_MidnightBlue());
colors->set_Light1(System::Drawing::Color::get_PaleGreen());
colors->set_Dark2(System::Drawing::Color::get_Indigo());
colors->set_Light2(System::Drawing::Color::get_Khaki());

colors->set_Accent1(System::Drawing::Color::get_OrangeRed());
colors->set_Accent2(System::Drawing::Color::get_LightSalmon());
colors->set_Accent3(System::Drawing::Color::get_Yellow());
colors->set_Accent4(System::Drawing::Color::get_Gold());
colors->set_Accent5(System::Drawing::Color::get_BlueViolet());
colors->set_Accent6(System::Drawing::Color::get_DarkViolet());

// طبق ألوانًا مخصصة على الروابط في حالتي النقر وعدم النقر.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## انظر أيضًا

* Class [ThemeColors](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
