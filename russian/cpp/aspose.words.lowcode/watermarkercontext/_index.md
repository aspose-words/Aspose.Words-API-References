---
title: "Aspose::Words::LowCode::WatermarkerContext class"
linktitle: "WatermarkerContext"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::LowCode::WatermarkerContext class. Контекст водяного знака документа на C++."
type: docs
weight: 1875
url: /ru/cpp/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class


[Document](../../aspose.words/document/) watermarker context.

```cpp
class WatermarkerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [get_ImageWatermark](./get_imagewatermark/)() const | Байты изображения, используемые в качестве водяного знака. |
| [get_ImageWatermarkOptions](./get_imagewatermarkoptions/)() const | Параметры текстового водяного знака. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Параметры макета [Document](../../aspose.words/document/) используемые процессором. |
| [get_TextWatermark](./get_textwatermark/)() const | Текст, используемый в качестве водяного знака. |
| [get_TextWatermarkOptions](./get_textwatermarkoptions/)() const | Параметры для изображения водяного знака. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Обратный вызов предупреждения, используемый процессором. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Настройки [Font](../../aspose.words/font/) используемые процессором. |
| [set_ImageWatermark](./set_imagewatermark/)(const System::ArrayPtr\<uint8_t\>\&) | Байты изображения, используемые в качестве водяного знака. |
| [set_TextWatermark](./set_textwatermark/)(const System::String\&) | Текст, используемый в качестве водяного знака. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Обратный вызов предупреждения, используемый процессором. |
| static [Type](./type/)() |  |
| [WatermarkerContext](./watermarkercontext/)() |  |
## См. также

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
