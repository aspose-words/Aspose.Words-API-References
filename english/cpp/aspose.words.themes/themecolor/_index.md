---
title: Aspose::Words::Themes::ThemeColor enum
linktitle: ThemeColor
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Themes::ThemeColor enum. Specifies the theme colors for document themes. To learn more, visit the Working with Styles and Themes documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.themes/themecolor/
---
## ThemeColor enum


Specifies the theme colors for document themes. 
To learn more, visit the [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) documentation article.

```cpp
enum class ThemeColor : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Accent1 | 4 | Accent color 1. |
| Accent2 | 5 | Accent color 2. |
| Accent3 | 6 | Accent color 3. |
| Accent4 | 7 | Accent color 4. |
| Accent5 | 8 | Accent color 5. |
| Accent6 | 9 | Accent color 6. |
| Background1 | 14 | Background color 1. |
| Background2 | 15 | Background color 2. |
| Dark1 | 0 | Dark main color 1. |
| Dark2 | 2 | Dark main color 2. |
| FollowedHyperlink | 11 | Followed hyperlink color. |
| Hyperlink | 10 | Hyperlink color. |
| Light1 | 1 | Light main color 1. |
| Light2 | 3 | Light main color 2. |
| None | -1 | No color. |
| Text1 | 12 | Text color 1. |
| Text2 | 13 | Text color 2. |

## Remarks

 The specified theme color is a reference to one of the predefined theme colors, located in the document's Theme part, which allows color information to be set centrally in the document. 
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

Shows how to create and use themed style.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// Create some style with theme font properties.
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(ThemeFont::Major);
style->get_Font()->set_ThemeColor(ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```
## See Also

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
