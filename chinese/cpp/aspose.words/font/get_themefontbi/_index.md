---
title: "Aspose::Words::Font::get_ThemeFontBi 方法"
linktitle: "get_ThemeFontBi"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font::get_ThemeFontBi 方法。获取或设置在 C++ 中右到左语言文档的应用字体方案中与此 Font 对象关联的主题字体。"
type: docs
weight: 51000
url: /zh/cpp/aspose.words/font/get_themefontbi/
---
## Font::get_ThemeFontBi method


获取或设置在右到左语言文档中与此 [Font](../) 对象关联的应用字体方案中的主题字体。

```cpp
Aspose::Words::Themes::ThemeFont Aspose::Words::Font::get_ThemeFontBi()
```


## 示例



展示如何使用主题字体和颜色。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 为语言默认使用定义字体。
doc->get_Theme()->get_MinorFonts()->set_Latin(u"Algerian");
doc->get_Theme()->get_MinorFonts()->set_EastAsian(u"Aharoni");
doc->get_Theme()->get_MinorFonts()->set_ComplexScript(u"Andalus");

System::SharedPtr<Aspose::Words::Font> font = doc->get_Styles()->idx_get(u"Normal")->get_Font();
std::cout << System::String::Format(u"Originally the Normal style theme color is: {0} and RGB color is: {1}\n", font->get_ThemeColor(), font->get_Color()) << std::endl;

// 我们可以使用主题字体和颜色来替代默认值。
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Minor);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent2);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::Minor, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::Accent2, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// 有多种方式可以重置它们的字体和颜色。
// 1 - 通过设置 ThemeFont.None/ThemeColor.None：
font->set_ThemeFont(Aspose::Words::Themes::ThemeFont::None);
font->set_ThemeColor(Aspose::Words::Themes::ThemeColor::None);

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Algerian", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Algerian", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Andalus", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Aharoni", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Algerian", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, font->get_Color());

// 2 - 通过设置非主题的字体/颜色名称：
font->set_Name(u"Arial");
font->set_Color(System::Drawing::Color::get_Blue());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFont());
ASSERT_EQ(u"Arial", font->get_Name());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontAscii());
ASSERT_EQ(u"Arial", font->get_NameAscii());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontBi());
ASSERT_EQ(u"Arial", font->get_NameBi());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontFarEast());
ASSERT_EQ(u"Arial", font->get_NameFarEast());

ASSERT_EQ(Aspose::Words::Themes::ThemeFont::None, font->get_ThemeFontOther());
ASSERT_EQ(u"Arial", font->get_NameOther());

ASSERT_EQ(Aspose::Words::Themes::ThemeColor::None, font->get_ThemeColor());
ASSERT_EQ(System::Drawing::Color::get_Blue().ToArgb(), font->get_Color().ToArgb());
```

## 另见

* Enum [ThemeFont](../../../aspose.words.themes/themefont/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
