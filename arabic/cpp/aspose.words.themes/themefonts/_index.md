---
title: "Aspose::Words::Themes::ThemeFonts class"
linktitle: "ThemeFonts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Themes::ThemeFonts class. يمثل مجموعة من الخطوط في مخطط الخطوط، مما يسمح بتحديد خطوط مختلفة للغات المختلفة Latin و EastAsian و ComplexScript. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.themes/themefonts/
---
## ThemeFonts class


يمثل مجموعة من الخطوط في مخطط الخطوط، مما يسمح بتحديد خطوط مختلفة للغات [Latin](./get_latin/)، [EastAsian](./get_eastasian/) و [ComplexScript](./get_complexscript/). لمعرفة المزيد، زر مقالة الوثائق [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class ThemeFonts : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_ComplexScript](./get_complexscript/)() | يحدد اسم الخط لأحرف ComplexScript. |
| [get_EastAsian](./get_eastasian/)() | يحدد اسم الخط لأحرف EastAsian. |
| [get_Latin](./get_latin/)() | يحدد اسم الخط لأحرف Latin. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ComplexScript](./set_complexscript/)(const System::String\&) | المحدد لـ [Aspose::Words::Themes::ThemeFonts::get_ComplexScript](./get_complexscript/). |
| [set_EastAsian](./set_eastasian/)(const System::String\&) | المحدد لـ [Aspose::Words::Themes::ThemeFonts::get_EastAsian](./get_eastasian/). |
| [set_Latin](./set_latin/)(const System::String\&) | المحدد لـ [Aspose::Words::Themes::ThemeFonts::get_Latin](./get_latin/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
