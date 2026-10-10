---
title: "Aspose::Words::TextWatermarkOptions class"
linktitle: "TextWatermarkOptions"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::TextWatermarkOptions class. 包含在添加文字水印时可指定的选项。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 72000
url: /zh/cpp/aspose.words/textwatermarkoptions/
---
## TextWatermarkOptions class


包含在添加文字水印时可以指定的选项。要了解更多，请访问 [Working with Watermark](https://docs.aspose.com/words/cpp/working-with-watermark/) 文档文章。

```cpp
class TextWatermarkOptions : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Color](./get_color/)() const | 获取或设置字体颜色。默认值为 **Silver**。 |
| [get_FontFamily](./get_fontfamily/)() const | 获取或设置字体族名称。默认值为 "Calibri"。 |
| [get_FontSize](./get_fontsize/)() const | 获取或设置字体大小。默认值为 0 - 自动。 |
| [get_IsSemitrasparent](./get_issemitrasparent/)() const | 获取或设置一个布尔值，用于控制水印的不透明度。默认值为 **true**。 |
| [get_Layout](./get_layout/)() const | 获取或设置水印的布局。默认值为 [Diagonal](../watermarklayout/)。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Color](./set_color/)(System::Drawing::Color) | 用于设置 [Aspose::Words::TextWatermarkOptions::get_Color](./get_color/)。 |
| [set_FontFamily](./set_fontfamily/)(const System::String\&) | 用于设置 [Aspose::Words::TextWatermarkOptions::get_FontFamily](./get_fontfamily/)。 |
| [set_FontSize](./set_fontsize/)(float) | 用于设置 [Aspose::Words::TextWatermarkOptions::get_FontSize](./get_fontsize/)。 |
| [set_IsSemitrasparent](./set_issemitrasparent/)(bool) | 用于设置 [Aspose::Words::TextWatermarkOptions::get_IsSemitrasparent](./get_issemitrasparent/)。 |
| [set_Layout](./set_layout/)(Aspose::Words::WatermarkLayout) | 用于设置 [Aspose::Words::TextWatermarkOptions::get_Layout](./get_layout/)。 |
| [TextWatermarkOptions](./textwatermarkoptions/)() |  |
| static [Type](./type/)() |  |

## 示例



展示如何创建文本水印。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// 添加纯文本水印。
doc->get_Watermark()->SetText(u"Aspose Watermark");

// 如果我们希望使用它作为水印来编辑文本格式，
// 我们可以在创建水印时传入 TextWatermarkOptions 对象来实现。
auto textWatermarkOptions = System::MakeObject<Aspose::Words::TextWatermarkOptions>();
textWatermarkOptions->set_FontFamily(u"Arial");
textWatermarkOptions->set_FontSize(36.0f);
textWatermarkOptions->set_Color(System::Drawing::Color::get_Black());
textWatermarkOptions->set_Layout(Aspose::Words::WatermarkLayout::Diagonal);
textWatermarkOptions->set_IsSemitrasparent(false);

doc->get_Watermark()->SetText(u"Aspose Watermark", textWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.TextWatermark.docx");

// 我们可以这样从文档中移除水印。
if (doc->get_Watermark()->get_Type() == Aspose::Words::WatermarkType::Text)
{
    doc->get_Watermark()->Remove();
}
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
