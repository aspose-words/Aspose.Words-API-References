---
title: "Aspose::Words::Themes::Theme class"
linktitle: "السمة"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Themes::Theme class. تمثّل سمة المستند، وتوفر الوصول إلى أجزاء السمة الرئيسية بما في ذلك MajorFonts و MinorFonts و Colors. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 1000
url: /ar/cpp/aspose.words.themes/theme/
---
## Theme class


يمثّل المستند [Theme](./)، ويوفر الوصول إلى أجزاء السمة الرئيسية بما في ذلك [MajorFonts](./get_majorfonts/)، [MinorFonts](./get_minorfonts/) و [Colors](./get_colors/). لمعرفة المزيد، زر مقالة الوثائق [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/).

```cpp
class Theme : public Aspose::Words::Drawing::Core::Dml::Themes::IThemeProvider,
              public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Colors](./get_colors/)() const | يسمح بتحديد مجموعة ألوان السمة للمستند. |
| [get_MajorFonts](./get_majorfonts/)() const | يسمح بتحديد مجموعة الخطوط الرئيسية للغات المختلفة. |
| [get_MinorFonts](./get_minorfonts/)() const | يسمح بتحديد مجموعة الخطوط الثانوية للغات المختلفة. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Theme](./theme/)() |  |
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
