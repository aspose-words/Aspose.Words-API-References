---
title: "Aspose::Words::LowCode::ReplacerContext clase"
linktitle: "ReplacerContext"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::ReplacerContext clase. Contexto de operación de buscar/reemplazar en C++."
type: docs
weight: 1292
url: /es/cpp/aspose.words.lowcode/replacercontext/
---
## ReplacerContext class


Contexto de la operación de buscar/reemplazar.

```cpp
class ReplacerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_FindReplaceOptions](./get_findreplaceoptions/)() const | Opciones de buscar/reemplazar. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opciones de diseño de [Documento](../../aspose.words/document/) usadas por el procesador. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Función de devolución de llamada de advertencia usada por el procesador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [ReplacerContext](./replacercontext/)() |  |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Función de devolución de llamada de advertencia usada por el procesador. |
| [SetReplacement](./setreplacement/)(const System::String\&, const System::String\&) | Establece el patrón y el reemplazo utilizados por la operación de buscar/reemplazar. |
| [SetReplacement](./setreplacement/)(const System::SharedPtr\<System::Text::RegularExpressions::Regex\>\&, const System::String\&) | Establece el patrón y el reemplazo utilizados por la operación de buscar/reemplazar. |
| static [Type](./type/)() |  |
## Ver también

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
