---
title: "فئة Aspose::Words::Themes::ThemeColors"
linktitle: "ThemeColors"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Themes::ThemeColors class. تمثّل مخطط ألوان سمة المستند الذي يحتوي على اثني عشر لونًا. كائن ThemeColors يحتوي على ستة ألوان تمييز، لونين داكنين، لونين فاتحين ولون لكل من الرابط التشعبي والرابط المتتبع في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


يمثّل مخطط ألوان سمة المستند الذي يحتوي على اثني عشر لونًا. كائن [ThemeColors](./) يحتوي على ستة ألوان تمييز، لونين داكنين، لونين فاتحين ولون لكل من الرابط التشعبي والرابط المتتبع.

```cpp
class ThemeColors : public System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [get_Accent1](./get_accent1/)() | يحدد اللون Accent 1. |
| [get_Accent2](./get_accent2/)() | يحدد اللون Accent 2. |
| [get_Accent3](./get_accent3/)() | يحدد اللون Accent 3. |
| [get_Accent4](./get_accent4/)() | يحدد اللون Accent 4. |
| [get_Accent5](./get_accent5/)() | يحدد اللون Accent 5. |
| [get_Accent6](./get_accent6/)() | يحدد اللون Accent 6. |
| [get_Dark1](./get_dark1/)() | يحدد اللون Dark 1. |
| [get_Dark2](./get_dark2/)() | يحدد اللون Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | يحدد اللون لرابط تشعبي تم النقر عليه. |
| [get_Hyperlink](./get_hyperlink/)() | يحدد اللون لرابط تشعبي. |
| [get_Light1](./get_light1/)() | يحدد اللون Light 1. |
| [get_Light2](./get_light2/)() | يحدد اللون Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | دالة تعيين لـ [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | مُعيّن لـ [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
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
