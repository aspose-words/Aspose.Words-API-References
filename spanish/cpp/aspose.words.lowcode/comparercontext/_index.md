---
title: "Clase Aspose::Words::LowCode::ComparerContext"
linktitle: "ComparerContext"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::ComparerContext. Contexto de comparador de documentos en C++."
type: docs
weight: 550
url: /es/cpp/aspose.words.lowcode/comparercontext/
---
## ComparerContext class


[Document](../../aspose.words/document/) comparer context.

```cpp
class ComparerContext : public Aspose::Words::LowCode::ProcessorContext
```

## Métodos

| Método | Descripción |
| --- | --- |
| [ComparerContext](./comparercontext/)() |  |
| [get_AcceptRevisions](./get_acceptrevisions/)() const | Indica si se deben aceptar revisiones en los documentos antes de compararlos. Si los documentos comparados contienen revisiones y este indicador está establecido en false, el procesador rechazará las revisiones. El valor predeterminado es **true**. |
| [get_Author](./get_author/)() const | El autor que se asignará a las revisiones creadas durante la comparación de documentos. |
| [get_CompareOptions](./get_compareoptions/)() const | Opciones utilizadas al comparar documentos. |
| [get_DateTime](./get_datetime/)() const | La fecha y hora asignadas a las revisiones creadas durante la comparación de documentos. |
| [get_FontSettings](../processorcontext/get_fontsettings/)() const | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [get_LayoutOptions](../processorcontext/get_layoutoptions/)() const | Opciones de diseño de [Documento](../../aspose.words/document/) usadas por el procesador. |
| [get_WarningCallback](../processorcontext/get_warningcallback/)() const | Función de devolución de llamada de advertencia usada por el procesador. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [ProcessorContext](../processorcontext/processorcontext/)() |  |
| [set_AcceptRevisions](./set_acceptrevisions/)(bool) | Indica si se deben aceptar revisiones en los documentos antes de compararlos. Si los documentos comparados contienen revisiones y este indicador está establecido en false, el procesador rechazará las revisiones. El valor predeterminado es **true**. |
| [set_Author](./set_author/)(const System::String\&) | El autor que se asignará a las revisiones creadas durante la comparación de documentos. |
| [set_DateTime](./set_datetime/)(System::DateTime) | La fecha y hora asignadas a las revisiones creadas durante la comparación de documentos. |
| [set_FontSettings](../processorcontext/set_fontsettings/)(const System::SharedPtr\<Aspose::Words::Fonts::FontSettings\>\&) | Configuraciones de [Fuente](../../aspose.words/font/) usadas por el procesador. |
| [set_WarningCallback](../processorcontext/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Función de devolución de llamada de advertencia usada por el procesador. |
| static [Type](./type/)() |  |
## Ver también

* Class [ProcessorContext](../processorcontext/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
