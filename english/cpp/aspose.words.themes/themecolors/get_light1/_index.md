---
title: get_Light1
second_title: Aspose.Words for C++ API Reference
description: Specifies color Light 1.
type: docs
weight: 131
url: /cpp/aspose.words.themes/themecolors/get_light1/
---
## ThemeColors.get_Light1 method


Specifies color Light 1.

```cpp
System::Drawing::Color Aspose::Words::Themes::ThemeColors::get_Light1()
```


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

