---
title: "Aspose::Words::Themes::ThemeColor 枚举"
linktitle: "ThemeColor"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Themes::ThemeColor 枚举。指定文档主题的主题颜色。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 4000
url: /zh/cpp/aspose.words.themes/themecolor/
---
## ThemeColor enum


指定文档主题的主题颜色。要了解更多，请访问 [Working with Styles and Themes](https://docs.aspose.com/words/cpp/working-with-styles-and-themes/) 文档文章。

```cpp
enum class ThemeColor
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| None | -1 | 无颜色。 |
| 暗色1 | 0 | 暗主颜色 1。 |
| 亮色1 | 1 | 亮主颜色 1。 |
| 暗色2 | 2 | 暗主颜色 2。 |
| 亮色2 | 3 | 亮主颜色 2。 |
| 强调色1 | 4 | 强调颜色 1。 |
| 强调色2 | 5 | 强调颜色 2。 |
| 强调色3 | 6 | 强调颜色 3。 |
| 强调色4 | 7 | 强调颜色 4。 |
| 强调色5 | 8 | 强调颜色 5。 |
| 强调色6 | 9 | 强调颜色 6。 |
| 超链接 | 10 | 超链接颜色。 |
| FollowedHyperlink | 11 | 已访问超链接颜色。 |
| 文本1 | 12 | 文本颜色 1。 |
| 文本2 | 13 | 文本颜色 2。 |
| 背景1 | 14 | 背景颜色 1。 |
| 背景2 | 15 | 背景颜色 2。 |


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


展示如何创建和使用主题样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln();

// 创建带有主题字体属性的样式。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"ThemedStyle");
style->get_Font()->set_ThemeFont(Aspose::Words::Themes::ThemeFont::Major);
style->get_Font()->set_ThemeColor(Aspose::Words::Themes::ThemeColor::Accent5);
style->get_Font()->set_TintAndShade(0.3);

builder->get_ParagraphFormat()->set_StyleName(u"ThemedStyle");
builder->Writeln(u"Text with themed style");
```

## 另见

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
