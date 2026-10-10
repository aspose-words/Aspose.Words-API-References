---
title: "Aspose::Words::Themes::ThemeColors class"
linktitle: "ThemeColors"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Themes::ThemeColors class. 表示文档主题的配色方案，包含十二种颜色。ThemeColors 对象包含六种强调色、两种深色、两种浅色，以及超链接和已访问超链接各一种颜色（C++）。"
type: docs
weight: 2000
url: /zh/cpp/aspose.words.themes/themecolors/
---
## ThemeColors class


表示文档主题的配色方案，包含十二种颜色。[ThemeColors](./) 对象包含六种强调色、两种深色、两种浅色，以及超链接和已访问超链接各一种颜色。

```cpp
class ThemeColors : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Accent1](./get_accent1/)() | 指定颜色 Accent 1。 |
| [get_Accent2](./get_accent2/)() | 指定颜色 Accent 2。 |
| [get_Accent3](./get_accent3/)() | 指定 Accent 3 颜色。 |
| [get_Accent4](./get_accent4/)() | 指定 Accent 4 颜色。 |
| [get_Accent5](./get_accent5/)() | 指定 Accent 5 颜色。 |
| [get_Accent6](./get_accent6/)() | 指定 Accent 6 颜色。 |
| [get_Dark1](./get_dark1/)() | 指定 Dark 1 颜色。 |
| [get_Dark2](./get_dark2/)() | 指定 Dark 2 颜色。 |
| [get_FollowedHyperlink](./get_followedhyperlink/)() | 指定已点击超链接的颜色。 |
| [get_Hyperlink](./get_hyperlink/)() | 指定超链接的颜色。 |
| [get_Light1](./get_light1/)() | 指定 Light 1 颜色。 |
| [get_Light2](./get_light2/)() | 指定 Light 2 颜色。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Accent1](./set_accent1/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent1](./get_accent1/)。 |
| [set_Accent2](./set_accent2/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent2](./get_accent2/)。 |
| [set_Accent3](./set_accent3/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent3](./get_accent3/)。 |
| [set_Accent4](./set_accent4/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent4](./get_accent4/)。 |
| [set_Accent5](./set_accent5/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent5](./get_accent5/)。 |
| [set_Accent6](./set_accent6/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Accent6](./get_accent6/)。 |
| [set_Dark1](./set_dark1/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Dark1](./get_dark1/)。 |
| [set_Dark2](./set_dark2/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Dark2](./get_dark2/)。 |
| [set_FollowedHyperlink](./set_followedhyperlink/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_FollowedHyperlink](./get_followedhyperlink/)。 |
| [set_Hyperlink](./set_hyperlink/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Hyperlink](./get_hyperlink/)。 |
| [set_Light1](./set_light1/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Light1](./get_light1/)。 |
| [set_Light2](./set_light2/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Themes::ThemeColors::get_Light2](./get_light2/)。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Themes](../)
* Library [Aspose.Words for C++](../../)
