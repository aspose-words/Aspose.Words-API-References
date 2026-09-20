---
title: "Aspose::Words::LowCode::Processor clase"
linktitle: "Processor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::Processor. Clase procesadora para realizar diferentes acciones de procesamiento de documentos en C++."
type: docs
weight: 1126
url: /es/cpp/aspose.words.lowcode/processor/
---
## Processor class


[Processor](./) class for performing different document processing actions.

```cpp
class Processor : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [Execute](./execute/)() | Ejecuta la acción del procesador. |
| [Execute](./execute/)(System::Threading::CancellationToken) | Ejecuta la acción del procesador permitiendo cancelar la tarea de procesamiento de documentos usando el token de cancelación especificado. |
| [From](./from/)(const System::String\&) | Especifica el documento de entrada para el procesamiento. |
| [From](./from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](./from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](./to/)(const System::String\&) | Especifica el archivo de salida para el procesador. |
| [To](./to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Especifica el archivo de salida para el procesador. |
| [To](./to/)(const System::String\&, Aspose::Words::SaveFormat) | Especifica el archivo de salida para el procesador. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Especifica el flujo de salida para el procesador. |
| [To](./to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Especifica el flujo de salida para el procesador. |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](./to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
