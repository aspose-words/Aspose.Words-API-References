---
title: Splitter Class
linktitle: Splitter
articleTitle: Splitter
second_title: Aspose.Words para .NET
description: Divida documentos fácilmente con la clase Aspose.Words.LowCode.Splitter. Utilice métodos versátiles para una gestión precisa de documentos y una mayor eficiencia del flujo de trabajo.
type: docs
weight: 4420
url: /es/net/aspose.words.lowcode/splitter/
---
## Splitter class

Proporciona métodos destinados a dividir los documentos en partes utilizando diferentes criterios.

```csharp
public class Splitter : Processor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.lowcode/splitter/create/)(*[SplitterContext](../splittercontext/)*) | Crea una nueva instancia del procesador divisor. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Ejecutar la acción del procesador. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el archivo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el archivo de salida para el procesador. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_4)(*string, string, int, int*) | Extrae un rango específico de páginas de un archivo de documento y las guarda en un nuevo archivo. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrae un rango específico de páginas de un flujo de documentos y guarda las páginas extraídas en un flujo de salida utilizando el formato de guardado especificado. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrae un rango específico de páginas de un flujo de documentos y guarda las páginas extraídas en un flujo de salida utilizando el formato de guardado especificado. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_2)(*string, string, [SaveFormat](../../aspose.words/saveformat/), int, int*) | Extrae un rango específico de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo utilizando el formato de guardado especificado. |
| static [ExtractPages](../../aspose.words.lowcode/splitter/extractpages/#extractpages_3)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), int, int*) | Extrae un rango específico de páginas de un archivo de documento y guarda las páginas extraídas en un nuevo archivo utilizando el formato de guardado especificado. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_2)(*string, string*) | Elimina las páginas vacías del documento y guarda el resultado. Devuelve una lista de los números de página eliminados. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Elimina las páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida con el formato de guardado especificado. Devuelve una lista de los números de página eliminados. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_1)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Elimina las páginas en blanco de un documento proporcionado en un flujo de entrada y guarda el documento actualizado en un flujo de salida con el formato de guardado especificado. Devuelve una lista de los números de página eliminados. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Elimina las páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de los números de página eliminados. |
| static [RemoveBlankPages](../../aspose.words.lowcode/splitter/removeblankpages/#removeblankpages_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Elimina las páginas vacías del documento y guarda la salida en el formato especificado. Devuelve una lista de los números de página eliminados. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split)(*Stream, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divide un documento de un flujo de entrada en varias partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_1)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divide un documento de un flujo de entrada en varias partes según las opciones de división especificadas y devuelve las partes resultantes como una matriz de flujos en el formato de guardado especificado. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_2)(*string, string, [SplitOptions](../splitoptions/)*) | Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos. El formato del archivo de salida se determina por la extensión del nombre del archivo de salida. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_3)(*string, string, [SaveFormat](../../aspose.words/saveformat/), [SplitOptions](../splitoptions/)*) | Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado. |
| static [Split](../../aspose.words.lowcode/splitter/split/#split_4)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), [SplitOptions](../splitoptions/)*) | Divide un documento en varias partes según las opciones de división especificadas y guarda las partes resultantes en archivos en el formato de guardado especificado. |

### Ver también

* class [Processor](../processor/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
