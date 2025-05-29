---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words para .NET
description: Convierta fácilmente varios tipos de documentos con Aspose.Words.LowCode.Converter. Simplifique su flujo de trabajo con una sola línea de código para una integración perfecta.
type: docs
weight: 4230
url: /es/net/aspose.words.lowcode/converter/
---
## Converter class

Representa un grupo de métodos destinados a convertir una variedad de diferentes tipos de documentos utilizando una sola línea de código.

```csharp
public class Converter : Processor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Crea una nueva instancia del procesador del convertidor. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Crea una nueva instancia del procesador del convertidor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Ejecutar la acción del procesador. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el archivo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el archivo de salida para el procesador. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y sus extensiones. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y el formato del documento final. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convierte el documento de entrada dado en un único documento de salida utilizando flujos de entrada y salida especificados. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Convierte el documento de entrada dado en el documento de salida utilizando los nombres de archivo de entrada y salida especificados y sus opciones de carga y guardado. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convierte las páginas del documento especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de secuencias que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Convierte las páginas del documento especificado en imágenes en el formato especificado y devuelve una matriz de secuencias que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convierte las páginas del flujo de entrada especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Convierte las páginas del flujo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de flujos que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convierte las páginas del archivo de entrada especificado en imágenes utilizando las opciones de guardado especificadas y devuelve una matriz de secuencias que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Convierte las páginas del archivo de entrada especificado en imágenes en el formato especificado y devuelve una matriz de secuencias que contienen las imágenes. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Convierte las páginas del flujo de entrada especificado en imágenes utilizando las opciones de carga y guardado proporcionadas, y devuelve una matriz de flujos que contienen las imágenes. |

## Observaciones

Los archivos o secuencias de entrada y salida especificados, junto con el formato de guardado deseado, , se utilizan para convertir el documento de entrada dado de un formato en el documento de salida del otro formato especificado.

La funcionalidad de conversión admite más de 35 formatos de archivos diferentes.

El[`ConvertToImages`](./converttoimages/)Este grupo de métodos está diseñado para transformar documentos en imágenes, donde cada página se convierte en un archivo de imagen independiente. Estos métodos también convierten documentos PDF directamente a formatos de página fija sin cargarlos en el modelo del documento, lo que mejora el rendimiento y la precisión.

Con[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), puede especificar un conjunto particular de páginas para convertir en imágenes.

### Ver también

* class [Processor](../processor/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
