---
title: get_ThemeFontAscii
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this Font object.
type: docs
weight: 638
url: /cpp/aspose.words/font/get_themefontascii/
---
## Font::get_ThemeFontAscii method


Gets or sets the theme font used for Latin text (characters with character codes from 0 (zero) through 127) in the applied font scheme that is associated with this [Font](../) object.

```cpp
Aspose::Words::Themes::ThemeFont Aspose::Words::Font::get_ThemeFontAscii()
```


## Examples



Shows how to work with theme fonts and colors. 
```cpp
auto doc = MakeObject<Document>();

// Define fonts for languages uses by default.
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

SharedPtr<Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color())
          << std::endl;

// We can use theme font and color instead of default values.
font->set_ThemeFont(ThemeFont::Minor);
font->set_ThemeColor(ThemeColor::Accent2);

ASSERT_EQ(ThemeFont::Minor, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(ThemeFont::Minor, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(ThemeFont::Minor, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(ThemeFont::Minor, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(ThemeFont::Minor, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(ThemeColor::Accent2, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// There are several ways of reset them font and color.
// 1 -  By setting ThemeFont.None/ThemeColor.None:
font->set_ThemeFont(ThemeFont::None);
font->set_ThemeColor(ThemeColor::None);

ASSERT_EQ(ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(ThemeColor::None, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// 2 -  By setting non-theme font/color names:
font->set_Name(u"Arial");
font->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Arial", font->get_Name());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Arial", font->get_NameAscii());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Arial", font->get_NameBi());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Arial", font->get_NameFarEast());

ASSERT_EQ(ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Arial", font->get_NameOther());

ASSERT_EQ(ThemeColor::None, font->get_ThemeColor());
ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), font->get_Color().ToArgb());
```

## See Also

* Enum [ThemeFont](../../../aspose.words.themes/themefont/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
