---
title: "Aspose::Words::Document::get_Theme طريقة"
linktitle: "get_Theme"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Document::get_Theme طريقة. يحصل على كائن Theme لهذا المستند في C++."
type: docs
weight: 53000
url: /ar/cpp/aspose.words/document/get_theme/
---
## Document::get_Theme method


يحصل على كائن [Theme](./) لهذا المستند.

```cpp
System::SharedPtr<Aspose::Words::Themes::Theme> Aspose::Words::Document::get_Theme()
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

* Class [Theme](../../../aspose.words.themes/theme/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
