---
title: Aspose::Words::LowCode::WatermarkerContext class
linktitle: WatermarkerContext
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::LowCode::WatermarkerContext class. Document watermarker context in C++.'
type: docs
weight: 1875
url: /cpp/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class


[Document](../../aspose.words/document/) watermarker context.

```cpp
class WatermarkerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Methods

| Method | Description |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | [Font](../../aspose.words/font/) settings used by the processor. |
| [get_ImageWatermark](./get_imagewatermark/)() const | Image bytes to be used as a watermark. |
| [get_ImageWatermarkOptions](./get_imagewatermarkoptions/)() const | Options for the text watermark. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | [Document](../../aspose.words/document/) layout options used by the processor. |
| [get_TextWatermark](./get_textwatermark/)() const | Text to be used as a watermark. |
| [get_TextWatermarkOptions](./get_textwatermarkoptions/)() const | Options for the image watermark. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Warning callback used by the processor. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | [Font](../../aspose.words/font/) settings used by the processor. |
| [set_ImageWatermark](./set_imagewatermark/)(const System::ArrayPtr\<uint8_t\>\&) | Image bytes to be used as a watermark. |
| [set_ImageWatermarkOptions](./set_imagewatermarkoptions/)(const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) | Options for the text watermark. |
| [set_TextWatermark](./set_textwatermark/)(const System::String\&) | Text to be used as a watermark. |
| [set_TextWatermarkOptions](./set_textwatermarkoptions/)(const System::SharedPtr\<Aspose::Words::TextWatermarkOptions\>\&) | Options for the image watermark. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Warning callback used by the processor. |
| static [Type](./type/)() |  |
## See Also

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
