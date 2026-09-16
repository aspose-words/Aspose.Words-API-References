---
title: "Aspose::Words::Font class"
linktitle: "字体"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Font 类。包含对象的字体属性（字体名称、字体大小、颜色等）。要了解更多，请访问 C++ 文档文章。"
type: docs
weight: 29000
url: /zh/cpp/aspose.words/font/
---
## Font class


包含对象的字体属性（字体名称、字体大小、颜色等）。要了解更多信息，请访问 [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) 文档文章。

```cpp
class Font : public Aspose::Words::IBorderAttrSource,
             public Aspose::Words::IShadingAttrSource,
             public Aspose::Words::Drawing::Core::IFillable
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | 重置为默认字体格式。 |
| [get_AllCaps](./get_allcaps/)() | 如果字体格式为全大写字母，则为 True。 |
| [get_AutoColor](./get_autocolor/)() | 返回用于“自动颜色”的文本当前计算颜色（黑色或白色）。如果颜色不是“auto”，则返回 [Color](./get_color/)。 |
| [get_Bidi](./get_bidi/)() | 指定此运行的内容是否应具有从右到左的特性。 |
| [get_Bold](./get_bold/)() | 如果字体设置为粗体，则为 True。 |
| [get_BoldBi](./get_boldbi/)() | 如果从右到左的文本格式为粗体，则为 True。 |
| [get_Border](./get_border/)() | 返回一个指定字体边框的 [Border](../border/) 对象。 |
| [get_Color](./get_color/)() | 获取或设置字体颜色。 |
| [get_ComplexScript](./get_complexscript/)() | 指定在确定此运行的格式时，无论其 Unicode 字符值如何，是否应将此运行的内容视为复杂脚本文本。 |
| [get_DoubleStrikeThrough](./get_doublestrikethrough/)() | 如果字体格式为双删除线文本，则为 True。 |
| [get_Emboss](./get_emboss/)() | 如果字体格式为浮雕效果，则为 True。 |
| [get_EmphasisMark](./get_emphasismark/)() | 获取或设置应用于此格式的强调标记。 |
| [get_Engrave](./get_engrave/)() | 如果字体格式为雕刻效果，则为 True。 |
| [get_Fill](./get_fill/)() | 获取 [Font](./) 的填充格式。 |
| [get_Hidden](./get_hidden/)() | 如果字体被格式化为隐藏文本，则为 True。 |
| [get_HighlightColor](./get_highlightcolor/)() | 获取或设置突出显示（标记）颜色。 |
| [get_Italic](./get_italic/)() | 如果字体设置为斜体，则为 True。 |
| [get_ItalicBi](./get_italicbi/)() | 如果从右到左的文本被格式化为斜体，则为 True。 |
| [get_Kerning](./get_kerning/)() | 获取或设置字距调整开始的字体大小。 |
| [get_LineSpacing](./get_linespacing/)() | 返回此字体的行间距（以磅为单位）。 |
| [get_LocaleId](./get_localeid/)() | 获取或设置已格式化字符的区域标识符（语言）。 |
| [get_LocaleIdBi](./get_localeidbi/)() | 获取或设置已格式化的从右到左字符的区域标识符（语言）。 |
| [get_LocaleIdFarEast](./get_localeidfareast/)() | 获取或设置已格式化的亚洲字符的区域标识符（语言）。 |
| [get_Name](./get_name/)() | 获取或设置字体名称。 |
| [get_NameAscii](./get_nameascii/)() | 返回或设置用于拉丁文文本的字体（字符代码从 0（零）到 127）。 |
| [get_NameBi](./get_namebi/)() | 返回或设置右到左语言文档中字体的名称。 |
| [get_NameFarEast](./get_namefareast/)() | 返回或设置东亚字体名称。 |
| [get_NameOther](./get_nameother/)() | 返回或设置用于字符代码从 128 到 255 的字符的字体。 |
| [get_NoProofing](./get_noproofing/)() | 当已格式化的字符不进行拼写检查时为 True。 |
| [get_NumberSpacing](./get_numberspacing/)() | 获取或设置所显示数字的间距类型。 |
| [get_Outline](./get_outline/)() | 如果字体被格式化为轮廓，则为 True。 |
| [get_Position](./get_position/)() | 获取或设置文本相对于基线的位置（以磅为单位）。正数会提升文本，负数会降低文本。 |
| [get_Scaling](./get_scaling/)() | 获取或设置字符宽度的百分比缩放。 |
| [get_Shading](./get_shading/)() | 返回一个指向字体阴影格式的 [Shading](../shading/) 对象。 |
| [get_Shadow](./get_shadow/)() | 如果字体被格式化为带阴影，则为 True。 |
| [get_Size](./get_size/)() | 获取或设置字体大小（磅）。 |
| [get_SizeBi](./get_sizebi/)() | 获取或设置在右到左文档中使用的字体大小（磅）。 |
| [get_SmallCaps](./get_smallcaps/)() | 如果字体被格式化为小型大写字母，则为 True。 |
| [get_SnapToGrid](./get_snaptogrid/)() | 指定在布局时当前字体是否应使用文档网格的每行字符设置。 |
| [get_Spacing](./get_spacing/)() | 返回或设置字符之间的间距（以点为单位）。 |
| [get_StrikeThrough](./get_strikethrough/)() | 如果字体被格式化为删除线文本，则为 True。 |
| [get_Style](./get_style/)() | 获取或设置应用于此格式的字符样式。 |
| [get_StyleIdentifier](./get_styleidentifier/)() | 获取或设置应用于此格式的字符样式的与区域设置无关的样式标识符。 |
| [get_StyleName](./get_stylename/)() | 获取或设置应用于此格式的字符样式的名称。 |
| [get_Subscript](./get_subscript/)() | 如果字体被格式化为下标，则为 True。 |
| [get_Superscript](./get_superscript/)() | 如果字体被格式化为上标，则为 True。 |
| [get_TextEffect](./get_texteffect/)() | 获取或设置字体动画效果。 |
| [get_ThemeColor](./get_themecolor/)() | 获取或设置与此 [Font](./) 对象关联的已应用配色方案中的主题颜色。 |
| [get_ThemeFont](./get_themefont/)() | 获取或设置与此 [Font](./) 对象关联的已应用字体方案中的主题字体。 |
| [get_ThemeFontAscii](./get_themefontascii/)() | 获取或设置与此 [Font](./) 对象关联的已应用字体方案中用于拉丁文本（字符代码从 0（零）到 127）的主题字体。 |
| [get_ThemeFontBi](./get_themefontbi/)() | 获取或设置在从右到左语言文档中，与此 [Font](./) 对象关联的已应用字体方案中的主题字体。 |
| [get_ThemeFontFarEast](./get_themefontfareast/)() | 获取或设置与此 [Font](./) 对象关联的已应用字体方案中的东亚主题字体。 |
| [get_ThemeFontOther](./get_themefontother/)() | 获取或设置与此 [Font](./) 对象关联的已应用字体方案中用于字符代码从 128 到 255 的字符的主题字体。 |
| [get_TintAndShade](./get_tintandshade/)() | 获取或设置用于使颜色变亮或变暗的双精度值。 |
| [get_Underline](./get_underline/)() | 获取或设置应用于字体的下划线类型。 |
| [get_UnderlineColor](./get_underlinecolor/)() | 获取或设置应用于字体的下划线颜色。 |
| [GetType](./gettype/)() const override |  |
| [HasDmlEffect](./hasdmleffect/)(Aspose::Words::TextDmlEffect) | 检查是否已应用特定的 DrawingML 文本效果。 |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_AllCaps](./set_allcaps/)(bool) | 用于设置 [Aspose::Words::Font::get_AllCaps](./get_allcaps/) 的 Setter。 |
| [set_Bidi](./set_bidi/)(bool) | 用于设置 [Aspose::Words::Font::get_Bidi](./get_bidi/) 的 Setter。 |
| [set_Bold](./set_bold/)(bool) | 用于设置 [Aspose::Words::Font::get_Bold](./get_bold/) 的 Setter。 |
| [set_BoldBi](./set_boldbi/)(bool) | 用于设置 [Aspose::Words::Font::get_BoldBi](./get_boldbi/) 的 Setter。 |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Font::get_Color](./get_color/) 的 Setter。 |
| [set_ComplexScript](./set_complexscript/)(bool) | 用于设置 [Aspose::Words::Font::get_ComplexScript](./get_complexscript/) 的 Setter。 |
| [set_DoubleStrikeThrough](./set_doublestrikethrough/)(bool) | 用于设置 [Aspose::Words::Font::get_DoubleStrikeThrough](./get_doublestrikethrough/) 的 Setter。 |
| [set_Emboss](./set_emboss/)(bool) | 用于设置 [Aspose::Words::Font::get_Emboss](./get_emboss/) 的 Setter。 |
| [set_EmphasisMark](./set_emphasismark/)(Aspose::Words::EmphasisMark) | 用于设置 [Aspose::Words::Font::get_EmphasisMark](./get_emphasismark/)。 |
| [set_Engrave](./set_engrave/)(bool) | 用于设置 [Aspose::Words::Font::get_Engrave](./get_engrave/)。 |
| [set_Hidden](./set_hidden/)(bool) | 用于设置 [Aspose::Words::Font::get_Hidden](./get_hidden/)。 |
| [set_HighlightColor](./set_highlightcolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Font::get_HighlightColor](./get_highlightcolor/)。 |
| [set_Italic](./set_italic/)(bool) | 用于设置 [Aspose::Words::Font::get_Italic](./get_italic/)。 |
| [set_ItalicBi](./set_italicbi/)(bool) | 用于设置 [Aspose::Words::Font::get_ItalicBi](./get_italicbi/)。 |
| [set_Kerning](./set_kerning/)(double) | 用于设置 [Aspose::Words::Font::get_Kerning](./get_kerning/)。 |
| [set_LocaleId](./set_localeid/)(int32_t) | 用于设置 [Aspose::Words::Font::get_LocaleId](./get_localeid/)。 |
| [set_LocaleIdBi](./set_localeidbi/)(int32_t) | 用于设置 [Aspose::Words::Font::get_LocaleIdBi](./get_localeidbi/)。 |
| [set_LocaleIdFarEast](./set_localeidfareast/)(int32_t) | 用于设置 [Aspose::Words::Font::get_LocaleIdFarEast](./get_localeidfareast/)。 |
| [set_Name](./set_name/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_Name](./get_name/)。 |
| [set_NameAscii](./set_nameascii/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_NameAscii](./get_nameascii/)。 |
| [set_NameBi](./set_namebi/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_NameBi](./get_namebi/)。 |
| [set_NameFarEast](./set_namefareast/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_NameFarEast](./get_namefareast/)。 |
| [set_NameOther](./set_nameother/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_NameOther](./get_nameother/)。 |
| [set_NoProofing](./set_noproofing/)(bool) | 用于设置 [Aspose::Words::Font::get_NoProofing](./get_noproofing/)。 |
| [set_NumberSpacing](./set_numberspacing/)(Aspose::Words::NumSpacing) | 用于设置 [Aspose::Words::Font::get_NumberSpacing](./get_numberspacing/)。 |
| [set_Outline](./set_outline/)(bool) | 用于设置 [Aspose::Words::Font::get_Outline](./get_outline/)。 |
| [set_Position](./set_position/)(double) | 用于设置 [Aspose::Words::Font::get_Position](./get_position/)。 |
| [set_Scaling](./set_scaling/)(int32_t) | 用于设置 [Aspose::Words::Font::get_Scaling](./get_scaling/)。 |
| [set_Shadow](./set_shadow/)(bool) | 用于设置 [Aspose::Words::Font::get_Shadow](./get_shadow/)。 |
| [set_Size](./set_size/)(double) | 用于设置 [Aspose::Words::Font::get_Size](./get_size/)。 |
| [set_SizeBi](./set_sizebi/)(double) | 用于设置 [Aspose::Words::Font::get_SizeBi](./get_sizebi/)。 |
| [set_SmallCaps](./set_smallcaps/)(bool) | 用于设置 [Aspose::Words::Font::get_SmallCaps](./get_smallcaps/)。 |
| [set_SnapToGrid](./set_snaptogrid/)(bool) | 指定在布局时当前字体是否应使用文档网格的每行字符设置。 |
| [set_Spacing](./set_spacing/)(double) | 用于设置 [Aspose::Words::Font::get_Spacing](./get_spacing/)。 |
| [set_StrikeThrough](./set_strikethrough/)(bool) | 用于设置 [Aspose::Words::Font::get_StrikeThrough](./get_strikethrough/)。 |
| [set_Style](./set_style/)(const System::SharedPtr\<Aspose::Words::Style\>\&) | 用于设置 [Aspose::Words::Font::get_Style](./get_style/)。 |
| [set_StyleIdentifier](./set_styleidentifier/)(Aspose::Words::StyleIdentifier) | 用于设置 [Aspose::Words::Font::get_StyleIdentifier](./get_styleidentifier/)。 |
| [set_StyleName](./set_stylename/)(const System::String\&) | 用于设置 [Aspose::Words::Font::get_StyleName](./get_stylename/)。 |
| [set_Subscript](./set_subscript/)(bool) | 用于设置 [Aspose::Words::Font::get_Subscript](./get_subscript/)。 |
| [set_Superscript](./set_superscript/)(bool) | 用于设置 [Aspose::Words::Font::get_Superscript](./get_superscript/)。 |
| [set_TextEffect](./set_texteffect/)(Aspose::Words::TextEffect) | 用于设置 [Aspose::Words::Font::get_TextEffect](./get_texteffect/)。 |
| [set_ThemeColor](./set_themecolor/)(Aspose::Words::Themes::ThemeColor) | 用于设置 [Aspose::Words::Font::get_ThemeColor](./get_themecolor/)。 |
| [set_ThemeFont](./set_themefont/)(Aspose::Words::Themes::ThemeFont) | 用于设置 [Aspose::Words::Font::get_ThemeFont](./get_themefont/)。 |
| [set_ThemeFontAscii](./set_themefontascii/)(Aspose::Words::Themes::ThemeFont) | 用于设置 [Aspose::Words::Font::get_ThemeFontAscii](./get_themefontascii/)。 |
| [set_ThemeFontBi](./set_themefontbi/)(Aspose::Words::Themes::ThemeFont) | 用于设置 [Aspose::Words::Font::get_ThemeFontBi](./get_themefontbi/)。 |
| [set_ThemeFontFarEast](./set_themefontfareast/)(Aspose::Words::Themes::ThemeFont) | 用于设置 [Aspose::Words::Font::get_ThemeFontFarEast](./get_themefontfareast/)。 |
| [set_ThemeFontOther](./set_themefontother/)(Aspose::Words::Themes::ThemeFont) | 用于设置 [Aspose::Words::Font::get_ThemeFontOther](./get_themefontother/)。 |
| [set_TintAndShade](./set_tintandshade/)(double) | 用于设置 [Aspose::Words::Font::get_TintAndShade](./get_tintandshade/)。 |
| [set_Underline](./set_underline/)(Aspose::Words::Underline) | 用于设置 [Aspose::Words::Font::get_Underline](./get_underline/)。 |
| [set_UnderlineColor](./set_underlinecolor/)(System::Drawing::Color) | 用于设置 [Aspose::Words::Font::get_UnderlineColor](./get_underlinecolor/)。 |
| static [Type](./type/)() |  |
## 备注


您不能直接创建 [Font](./) 类的实例。您只需使用 [Font](./) 来访问各种对象（如 [Run](../run/)、[Paragraph](../paragraph/)、[Style](../style/)、[DocumentBuilder](../documentbuilder/)）的字体属性。

## 示例



展示如何在文档中插入被边框包围的字符串。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


展示如何使用其字体属性格式化文本运行。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto run = System::MakeObject<Aspose::Words::Run>(doc, u"Hello world!");

System::SharedPtr<Aspose::Words::Font> font = run->get_Font();
font->set_Name(u"Courier New");
font->set_Size(36);
font->set_HighlightColor(System::Drawing::Color::get_Yellow());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);
doc->Save(get_ArtifactsDir() + u"Font.CreateFormattedRun.docx");
```


展示如何创建并使用带列表格式的段落样式。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// 创建自定义段落样式。
System::SharedPtr<Aspose::Words::Style> style = doc->get_Styles()->Add(Aspose::Words::StyleType::Paragraph, u"MyStyle1");
style->get_Font()->set_Size(24);
style->get_Font()->set_Name(u"Verdana");
style->get_ParagraphFormat()->set_SpaceAfter(12);

// 创建列表，并确保使用此样式的段落将使用该列表。
style->get_ListFormat()->set_List(doc->get_Lists()->Add(Aspose::Words::Lists::ListTemplate::BulletDefault));
style->get_ListFormat()->set_ListLevelNumber(0);

// 将段落样式应用于文档生成器的当前段落，然后添加一些文本。
builder->get_ParagraphFormat()->set_Style(style);
builder->Writeln(u"Hello World: MyStyle1, bulleted list.");

// 将文档生成器的样式更改为没有列表格式的样式，并写入另一段落。
builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Normal"));
builder->Writeln(u"Hello World: Normal.");

builder->get_Document()->Save(get_ArtifactsDir() + u"Styles.ParagraphStyleBulletedList.docx");
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
