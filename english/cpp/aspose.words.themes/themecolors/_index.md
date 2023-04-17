---
title: Aspose::Words::Themes::ThemeColors class
linktitle: ThemeColors
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Themes::ThemeColors class. Represents the color scheme of the document theme which contains twelve colors. ThemeColors object contains six accent colors, two dark colors, two light colors and a color for each of a hyperlink and followed hyperlink in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


Represents the color scheme of the document theme which contains twelve colors. [ThemeColors](./) object contains six accent colors, two dark colors, two light colors and a color for each of a hyperlink and followed hyperlink.

```cpp
class ThemeColors : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Accent1](./get_accent1/)() | Specifies color Accent 1. |
| [get_Accent2](./get_accent2/)() | Specifies color Accent 2. |
| [get_Accent3](./get_accent3/)() | Specifies color Accent 3. |
| [get_Accent4](./get_accent4/)() | Specifies color Accent 4. |
| [get_Accent5](./get_accent5/)() | Specifies color Accent 5. |
| [get_Accent6](./get_accent6/)() | Specifies color Accent 6. |
| [get_Dark1](./get_dark1/)() | Specifies color Dark 1. |
| [get_Dark2](./get_dark2/)() | Specifies color Dark 2. |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | Specifies color for a clicked hyperlink. |
| [get_Hyperlink](./get_hyperlink/)() | Specifies color for a hyperlink. |
| [get_Light1](./get_light1/)() | Specifies color Light 1. |
| [get_Light2](./get_light2/)() | Specifies color Light 2. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/). |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/). |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/). |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/). |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/). |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/). |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/). |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/). |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/). |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/). |
| [set_Light1](./set_light1/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/). |
| [set_Light2](./set_light2/)(System::Drawing::Color) | Setter for [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/). |
| static [Type](./type/)() |  |

## Examples



Shows how to set custom colors and fonts for themes. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Theme colors.docx");

// The "Theme" object gives us access to the document theme, a source of default fonts and colors.
SharedPtr<Theme> theme = doc->get_Theme();

// Some styles, such as "Heading 1" and "Subtitle", will inherit these fonts.
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// Other languages may also have their custom fonts in this theme.
ASSERT_EQ(String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(String::Empty, theme->get_MinorFonts()->get_EastAsian());

// The "Colors" property contains the color palette from Microsoft Word,
// which appears when changing shading or font color.
// Apply custom colors to the color palette so we have easy access to them in Microsoft Word
// when we, for example, change the font color via "Home" -> "Font" -> "Font Color",
// or insert a shape, and then set a color for it via "Shape Format" -> "Shape Styles".
SharedPtr<ThemeColors> colors = theme->get_Colors();
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

// Apply custom colors to hyperlinks in their clicked and un-clicked states.
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(ArtifactsDir + u"Themes.CustomColorsAndFonts.docx");
```

## See Also

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
