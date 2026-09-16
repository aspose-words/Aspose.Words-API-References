---
title: "Aspose::Words::Themes::ThemeFonts::get_ComplexScript 方法"
linktitle: "get_ComplexScript"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Themes::ThemeFonts::get_ComplexScript 方法。指定 C++ 中 ComplexScript 字符的字体名称。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.themes/themefonts/get_complexscript/
---
## ThemeFonts::get_ComplexScript method


指定 ComplexScript 字符的字体名称。

```cpp
System::String Aspose::Words::Themes::ThemeFonts::get_ComplexScript()
```


## 示例



展示如何为主题设置自定义颜色和字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Theme colors.docx");

// “Theme” 对象让我们访问文档主题，它是默认字体和颜色的来源。
System::SharedPtr<Aspose::Words::Themes::Theme> theme = doc->get_Theme();

// 某些样式，例如 “Heading 1” 和 “Subtitle”，将继承这些字体。
theme->get_MajorFonts()->set_Latin(u"Courier New");
theme->get_MinorFonts()->set_Latin(u"Agency FB");

// 其他语言也可能在此主题中拥有其自定义字体。
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MajorFonts()->get_EastAsian());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_ComplexScript());
ASSERT_EQ(System::String::Empty, theme->get_MinorFonts()->get_EastAsian());

// “Colors” 属性包含来自 Microsoft Word 的颜色调色板，
// 该调色板在更改底纹或字体颜色时出现。
// 将自定义颜色应用到颜色调色板，以便在 Microsoft Word 中轻松访问它们
// 例如，当我们通过 “Home” → “Font” → “Font Color” 更改字体颜色时，
// 或插入形状，然后通过 “Shape Format” → “Shape Styles” 为其设置颜色。
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

// 在超链接的已点击和未点击状态下应用自定义颜色。
colors->set_Hyperlink(System::Drawing::Color::get_Black());
colors->set_FollowedHyperlink(System::Drawing::Color::get_Gray());

doc->Save(get_ArtifactsDir() + u"Themes.CustomColorsAndFonts.docx");
```

## 另见

* Class [ThemeFonts](../)
* Namespace [Aspose::Words::Themes](../../)
* Library [Aspose.Words for C++](../../../)
