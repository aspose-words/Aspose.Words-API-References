---
title: "Aspose::Words::LowCode::WatermarkerContext 类"
linktitle: "WatermarkerContext"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::LowCode::WatermarkerContext 类。C++ 中的文档水印上下文。"
type: docs
weight: 1875
url: /zh/cpp/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class


[Document](../../aspose.words/document/) watermarker context.

```cpp
class WatermarkerContext : public Aspose::Words::LowCode::ProcessorContext
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [get_ImageWatermark](./get_imagewatermark/)() const | 用作水印的图像字节。 |
| [get_ImageWatermarkOptions](./get_imagewatermarkoptions/)() const | 文本水印的选项。 |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | 处理器使用的 [Document](../../aspose.words/document/) 布局选项。 |
| [get_TextWatermark](./get_textwatermark/)() const | 用作水印的文本。 |
| [get_TextWatermarkOptions](./get_textwatermarkoptions/)() const | 图像水印的选项。 |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | 处理器使用的警告回调。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | 处理器使用的 [Font](../../aspose.words/font/) 设置。 |
| [set_ImageWatermark](./set_imagewatermark/)(const System::ArrayPtr\<uint8_t\>\&) | 用作水印的图像字节。 |
| [set_TextWatermark](./set_textwatermark/)(const System::String\&) | 用作水印的文本。 |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 处理器使用的警告回调。 |
| static [Type](./type/)() |  |
| [WatermarkerContext](./watermarkercontext/)() |  |
## 另见

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
