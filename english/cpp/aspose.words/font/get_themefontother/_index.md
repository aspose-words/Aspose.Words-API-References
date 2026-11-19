---
title: Aspose::Words::Font::get_ThemeFontOther method
linktitle: get_ThemeFontOther
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Font::get_ThemeFontOther method. Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this Font object in C++.'
type: docs
weight: 59860
url: /cpp/aspose.words/font/get_themefontother/
---
## Font::get_ThemeFontOther method


Gets or sets the theme font used for characters with character codes from 128 through 255 in the applied font scheme that is associated with this [Font](../) object.

```cpp
Aspose::Words::Themes::ThemeFont Aspose::Words::Font::get_ThemeFontOther()
```

## Examples


Shows how to work with theme fonts and colors.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Define fonts for languages uses by default.
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

System::SharedPtr<Aspose::Words::Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << System::String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color()) << std::endl;

// We can use theme font and color instead of default values.
font->set_ThemeFont(ThemeFont::Minor);
font->set_ThemeColor(ThemeColor::Accent2);

ASSERT_EQ(font->get_ThemeFont(), ThemeFont::Minor);
ASSERT_EQ(font->get_Name(), u"Algerian");

ASSERT_EQ(font->get_ThemeFontAscii(), ThemeFont::Minor);
ASSERT_EQ(font->get_NameAscii(), u"Algerian");

ASSERT_EQ(font->get_ThemeFontBi(), ThemeFont::Minor);
ASSERT_EQ(font->get_NameBi(), u"Andalus");

ASSERT_EQ(font->get_ThemeFontFarEast(), ThemeFont::Minor);
ASSERT_EQ(font->get_NameFarEast(), u"Aharoni");

ASSERT_EQ(font->get_ThemeFontOther(), ThemeFont::Minor);
ASSERT_EQ(font->get_NameOther(), u"Algerian");

ASSERT_EQ(font->get_ThemeColor(), ThemeColor::Accent2);
ASPOSE_ASSERT_EQ(font->get_Color(), System::Drawing::Color::Empty);

// There are several ways of reset them font and color.
// 1 -  By setting ThemeFont.None/ThemeColor.None:
font->set_ThemeFont(ThemeFont::None);
font->set_ThemeColor(ThemeColor::None);

ASSERT_EQ(font->get_ThemeFont(), ThemeFont::None);
ASSERT_EQ(font->get_Name(), u"Algerian");

ASSERT_EQ(font->get_ThemeFontAscii(), ThemeFont::None);
ASSERT_EQ(font->get_NameAscii(), u"Algerian");

ASSERT_EQ(font->get_ThemeFontBi(), ThemeFont::None);
ASSERT_EQ(font->get_NameBi(), u"Andalus");

ASSERT_EQ(font->get_ThemeFontFarEast(), ThemeFont::None);
ASSERT_EQ(font->get_NameFarEast(), u"Aharoni");

ASSERT_EQ(font->get_ThemeFontOther(), ThemeFont::None);
ASSERT_EQ(font->get_NameOther(), u"Algerian");

ASSERT_EQ(font->get_ThemeColor(), ThemeColor::None);
ASPOSE_ASSERT_EQ(font->get_Color(), System::Drawing::Color::Empty);

// 2 -  By setting non-theme font/color names:
font->set_Name(u"Arial");
font->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(font->get_ThemeFont(), ThemeFont::None);
ASSERT_EQ(font->get_Name(), u"Arial");

ASSERT_EQ(font->get_ThemeFontAscii(), ThemeFont::None);
ASSERT_EQ(font->get_NameAscii(), u"Arial");

ASSERT_EQ(font->get_ThemeFontBi(), ThemeFont::None);
ASSERT_EQ(font->get_NameBi(), u"Arial");

ASSERT_EQ(font->get_ThemeFontFarEast(), ThemeFont::None);
ASSERT_EQ(font->get_NameFarEast(), u"Arial");

ASSERT_EQ(font->get_ThemeFontOther(), ThemeFont::None);
ASSERT_EQ(font->get_NameOther(), u"Arial");

ASSERT_EQ(font->get_ThemeColor(), ThemeColor::None);
ASSERT_EQ(font->get_Color().ToArgb(), System::Drawing::Color::get_Blue().ToArgb());
```
## See Also

* Enum [ThemeFont](../../../aspose.words.themes/themefont/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
