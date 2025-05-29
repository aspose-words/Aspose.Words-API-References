---
title: ReportBuilder Class
linktitle: ReportBuilder
articleTitle: ReportBuilder
second_title: Aspose.Words para .NET
description: Cree informes dinámicos fácilmente con Aspose.Words LowCode ReportBuilder. Utilice el motor de informes LINQ para completar las plantillas con datos sin problemas.
type: docs
weight: 4360
url: /es/net/aspose.words.lowcode/reportbuilder/
---
## ReportBuilder class

Proporciona métodos destinados a rellenar la plantilla con datos mediante el motor de informes LINQ.

```csharp
public class ReportBuilder : Processor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create)() | Crea una nueva instancia del procesador del generador de informes. |
| static [Create](../../aspose.words.lowcode/reportbuilder/create/#create_1)(*[ReportBuilderContext](../reportbuildercontext/)*) | Crea una nueva instancia del procesador del generador de informes. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Ejecutar la acción del procesador. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el archivo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el archivo de salida para el procesador. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_12)(*string, string, object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales, a partir de flujos de entrada y salida. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales, a partir de flujos de entrada y salida. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_13)(*string, string, object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_14)(*string, string, object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con opciones adicionales. Esta sobrecarga determina automáticamente el formato de guardado en función de la extensión del archivo de salida. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con el formato de salida especificado y opciones adicionales a partir de los flujos de archivos de entrada y salida especificados. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con una referencia de fuente de datos con nombre y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con el formato de salida especificado y opciones adicionales a partir de los flujos de archivos de entrada y salida especificados. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida específico y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object, string, [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de la fuente especificada, generando un informe completo con el formato de salida especificado, una referencia de fuente de datos con nombre y opciones adicionales. |
| static [BuildReport](../../aspose.words.lowcode/reportbuilder/buildreport/#buildreport_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes, generando un informe completo con un formato de salida específico y opciones adicionales. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes. Representa la salida en imágenes. |
| static [BuildReportToImages](../../aspose.words.lowcode/reportbuilder/buildreporttoimages/#buildreporttoimages_1)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), object[], string[], [ReportBuilderOptions](../reportbuilderoptions/)*) | Rellena el documento de plantilla con datos de múltiples fuentes. Representa la salida en imágenes. |

### Ver también

* class [Processor](../processor/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
