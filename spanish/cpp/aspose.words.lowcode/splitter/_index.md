---
title: "Clase Aspose::Words::LowCode::Splitter"
linktitle: "Splitter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::Splitter. Proporciona métodos destinados a dividir los documentos en partes usando diferentes criterios en C++."
type: docs
weight: 1500
url: /es/cpp/aspose.words.lowcode/splitter/
---
## Splitter class


Proporciona métodos destinados a dividir los documentos en partes utilizando diferentes criterios.

```cpp
class Splitter : public Aspose::Words::LowCode::Processor
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::SplitterContext\>\&) | Crea una nueva instancia del procesador divisor. |
| [Execute](../processor/execute/)() | Ejecuta la acción del procesador. |
| [Execute](../processor/execute/)(System::Threading::CancellationToken) | Ejecuta la acción del procesador permitiendo cancelar la tarea de procesamiento de documentos usando el token de cancelación especificado. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, int32_t, int32_t) | Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo usando el formato de guardado especificado. |
| static [ExtractPages](./extractpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrae un rango especificado de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo usando el formato de guardado especificado. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, int32_t, int32_t) | Extrae un rango especificado de páginas de un flujo de documento y guarda las páginas extraídas en un flujo de salida usando el formato de guardado especificado. |
| static [ExtractPages](./extractpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, int32_t, int32_t) | Extrae un rango especificado de páginas de un flujo de documento y guarda las páginas extraídas en un flujo de salida usando el formato de guardado especificado. |
| [From](../processor/from/)(const System::String\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&) | Especifica el documento de entrada para el procesamiento. |
| [From](../processor/from/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Especifica el documento de entrada para el procesamiento. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&) | Elimina páginas vacías del documento y guarda la salida. Devuelve una lista de números de página que fueron eliminados. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Elimina páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de números de página que fueron eliminados. |
| static [RemoveBlankPages](./removeblankpages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Elimina páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de números de página que fueron eliminados. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Elimina páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida en el formato de guardado especificado. Devuelve una lista de números de página que fueron eliminados. |
| static [RemoveBlankPages](./removeblankpages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Elimina páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida en el formato de guardado especificado. Devuelve una lista de números de página que fueron eliminados. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida. |
| static [Split](./split/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado. |
| static [Split](./split/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento en múltiples partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento de un flujo de entrada en múltiples partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado. |
| static [Split](./split/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&, const System::SharedPtr\<Aspose::Words::LowCode::SplitOptions\>\&) | Divide un documento de un flujo de entrada en múltiples partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado. |
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
