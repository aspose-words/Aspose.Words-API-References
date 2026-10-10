---
title: "Clase Aspose::Words::LowCode::Converter"
linktitle: "Converter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::LowCode::Converter. Representa un conjunto de métodos destinados a convertir una variedad de diferentes tipos de documentos usando una sola línea de código en C++."
type: docs
weight: 600
url: /es/cpp/aspose.words.lowcode/converter/
---
## Converter class


Representa un conjunto de métodos destinados a convertir una variedad de diferentes tipos de documentos usando una sola línea de código.

```cpp
class Converter : public Aspose::Words::LowCode::Processor
```

## Métodos

| Método | Descripción |
| --- | --- |
| static [Convert](./convert/)(const System::String\&, const System::String\&) | Convierte el documento de entrada proporcionado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y sus extensiones. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Convierte el documento de entrada dado en el documento de salida usando los nombres de archivo de entrada y salida especificados y el formato final del documento. |
| static [Convert](./convert/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convierte el documento de entrada dado en el documento de salida usando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [Convert](./convert/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convierte el documento de entrada dado en el documento de salida usando los nombres de archivo de entrada y salida especificados y sus opciones de carga/guardado. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Convierte el documento de entrada dado en un único documento de salida usando los flujos de entrada y salida especificados. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convierte el documento de entrada dado en un único documento de salida usando los flujos de entrada y salida especificados. |
| static [Convert](./convert/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::SaveOptions\>\&) | Convierte el documento de entrada dado en un único documento de salida usando los flujos de entrada y salida especificados. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&) | Convierte las páginas del archivo de entrada especificado en archivos de imagen. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, Aspose::Words::SaveFormat) | Convierte las páginas del archivo de entrada especificado en archivos de imagen en el formato especificado. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del archivo de entrada especificado en archivos de imagen usando las opciones de guardado especificadas. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del archivo de entrada especificado en archivos de imagen usando las opciones de carga y guardado proporcionadas. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, Aspose::Words::SaveFormat) | Convierte las páginas del archivo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del archivo de entrada especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, Aspose::Words::SaveFormat) | Convierte las páginas del flujo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del flujo de entrada especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del flujo de entrada especificado en imágenes usando las opciones de carga y guardado proporcionadas, y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, Aspose::Words::SaveFormat) | Convierte las páginas del documento especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](./converttoimages/)(const System::SharedPtr\<Aspose::Words::Document\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&) | Convierte las páginas del documento especificado en imágenes usando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes. |
| static [Create](./create/)() | Crea una nueva instancia del procesador convertidor. |
| static [Create](./create/)(const System::SharedPtr\<Aspose::Words::LowCode::ConverterContext\>\&) | Crea una nueva instancia del procesador convertidor. |
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
## Observaciones


Los archivos o flujos de entrada y salida especificados, junto con el formato de guardado deseado, se utilizan para convertir el documento de entrada dado de un formato en el documento de salida del otro formato especificado.

La funcionalidad de conversión admite más de 35 formatos de archivo diferentes.

El grupo de métodos [ConvertToImages()](../) está diseñado para transformar documentos en imágenes, con cada página convirtiéndose en un archivo de imagen separado. Estos métodos también convierten documentos PDF directamente a formatos de página fija sin cargarlos en el modelo de documento, lo que mejora tanto el rendimiento como la precisión.

Con [PageSet](../../aspose.words.saving/imagesaveoptions/get_pageset/), puedes especificar un conjunto particular de páginas para convertir en imágenes.
## Ver también

* Class [Processor](../processor/)
* Namespace [Aspose::Words::LowCode](../)
* Library [Aspose.Words for C++](../../)
