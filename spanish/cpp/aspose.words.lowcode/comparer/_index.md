---
title: "Aspose::Words::LowCode::Comparer clase"
linktitle: "Comparador"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Comparer clase. Proporciona métodos destinados a comparar documentos en C++."
type: docs
weight: 500
url: /es/cpp/aspose.words.lowcode/comparer/
---
## Comparer class


Proporciona métodos destinados a comparar documentos.

```cpp
class Comparer : public Aspose::Words::LowCode::Processor
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::String\&, const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos con opciones adicionales y guarda las diferencias en el archivo de salida especificado en el formato de guardado proporcionado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime) | Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime) | Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [Compare](./compare/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos cargados desde flujos con opciones adicionales y guarda las diferencias en el flujo de salida proporcionado en el formato de guardado especificado, produciendo cambios como una serie de revisiones de edición y formato. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen. |
| static [CompareToImages](./comparetoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime) | Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen. |
| static [CompareToImages](./comparetoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, const System::String\&, System::DateTime, const System::SharedPtr\<Aspose::Words::Comparing::CompareOptions\>\&) | Compara dos documentos y guarda las diferencias como imágenes. Cada elemento en la matriz devuelta representa una sola página de la salida renderizada como una imagen. |
| static [Create](./create/)() | Crea una nueva instancia del procesador convertidor. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ComparerContext\>\&) | Crea una nueva instancia del procesador comparador. |
| [Execute](../processor/execute/)() | Ejecuta la acción del procesador. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Ejecuta la acción del procesador permitiendo cancelar la tarea de procesamiento de documentos usando el token de cancelación especificado. |
| [From](../processor/from/)(const System::String\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [To](../processor/to/)(const System::String\&) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::String\&, System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::String\&, Aspose::Words::SaveFormat) | Especifica el archivo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Especifica el flujo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Especifica el flujo de salida para el procesador. |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) |  |
| [To](../processor/to/)(const System::SharedPtr\<System::Collections::Generic::List\<System::SharedPtr\<System::IO::Stream\>\>\>\&, Aspose::Words::SaveFormat) |  |
| static [Type](./type/)() |  |
## Ver también

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
