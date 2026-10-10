---
title: "Clase Aspose::Words::LowCode::WatermarkerContext"
linktitle: "WatermarkerContext"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::WatermarkerContext. Contexto de marcador de agua de documento en C++."
type: docs
weight: 1875
url: /es/cpp/aspose.words.lowcode/watermarkercontext/
---
## WatermarkerContext class


[Document](../../aspose.words/document/) watermarker context.

```cpp
class WatermarkerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [get_ImageWatermark](./get_imagewatermark/)() const | Bytes de imagen que se usarán como marca de agua. |
| [get_ImageWatermarkOptions](./get_imagewatermarkoptions/)() const | Opciones para la marca de agua de texto. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opciones de diseño de [Documento](../../aspose.words/document/) usadas por el procesador. |
| [get_TextWatermark](./get_textwatermark/)() const | Texto que se usará como marca de agua. |
| [get_TextWatermarkOptions](./get_textwatermarkoptions/)() const | Opciones para la marca de agua de imagen. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Función de devolución de llamada de advertencia usada por el procesador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [set_ImageWatermark](./set_imagewatermark/)(const System::ArrayPtr\<uint8_t\>\&) | Bytes de imagen que se usarán como marca de agua. |
| [set_TextWatermark](./set_textwatermark/)(const System::String\&) | Texto que se usará como marca de agua. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Función de devolución de llamada de advertencia usada por el procesador. |
| static [Type](./type/)() |  |
| [WatermarkerContext](./watermarkercontext/)() |  |
## Ver también

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
