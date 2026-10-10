---
title: "Clase Aspose::Words::LowCode::Merger"
linktitle: "Merger"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::Merger. Representa un conjunto de métodos destinados a combinar una variedad de diferentes tipos de documentos en un único documento de salida en C++."
type: docs
weight: 1000
url: /es/cpp/aspose.words.lowcode/merger/
---
## Merger class


Representa un conjunto de métodos destinados a combinar una variedad de diferentes tipos de documentos en un único documento de salida.

```cpp
class Merger : public Aspose::Words::LowCode::Processor
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Create](./create/)() | Crea una nueva instancia del procesador de combinación de correo. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::MergerContext\>\&) | Crea una nueva instancia del procesador de combinación de correo. |
| [Execute](../processor/execute/)() | Ejecuta la acción del procesador. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Ejecuta la acción del procesador permitiendo cancelar la tarea de procesamiento de documentos usando el token de cancelación especificado. |
| [From](../processor/from/)(const System::String\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados mediante [KeepSourceFormatting](../mergeformatmode/). |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, Aspose::Words::SaveFormat, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados y el formato final del documento. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [Merge](./merge/)(const System::String\&, const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento y devuelve una instancia de [Document](../../aspose.words/document/) del documento final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::String\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento y devuelve una instancia de [Document](../../aspose.words/document/) del documento final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Document\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento y devuelve una instancia de [Document](../../aspose.words/document/) del documento final. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::SaveFormat) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los flujos de entrada y salida especificados y el formato final del documento. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los flujos de entrada y salida especificados y las opciones de guardado. |
| static [Merge](./merge/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los flujos de entrada y salida especificados y las opciones de guardado. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento y devuelve una instancia de [Document](../../aspose.words/document/) del documento final. |
| static [Merge](./merge/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento y devuelve una instancia de [Document](../../aspose.words/document/) del documento final. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados y las opciones de guardado. Renderiza la salida a imágenes. |
| static [MergeToImages](./mergetoimages/)(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) | Fusiona los flujos de documentos de entrada proporcionados en un único documento de salida usando las opciones de guardado de imagen especificadas. Renderiza la salida a imágenes. |
| [To](../processor/to/)(const System::String\&) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Especifica el flujo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Especifica el flujo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Observaciones


Los archivos o flujos de entrada y salida especificados, junto con las opciones de fusión y guardado deseadas, se utilizan para fusionar los documentos de entrada proporcionados en un único documento de salida.

La funcionalidad de fusión admite más de 35 formatos de archivo diferentes.
## Ver también

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
