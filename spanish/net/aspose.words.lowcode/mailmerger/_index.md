---
title: MailMerger Class
linktitle: MailMerger
articleTitle: MailMerger
second_title: Aspose.Words para .NET
description: Descubra Aspose.Words.LowCode.MailMerger. Complete plantillas con datos fácilmente mediante técnicas de combinación de correspondencia sencillas y avanzadas para una automatización fluida de documentos.
type: docs
weight: 4270
url: /es/net/aspose.words.lowcode/mailmerger/
---
## MailMerger class

Proporciona métodos destinados a llenar la plantilla con datos mediante operaciones de combinación de correspondencia simple y combinación de correspondencia con regiones.

```csharp
public class MailMerger : Processor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.lowcode/mailmerger/create/)(*[MailMergerContext](../mailmergercontext/)*) | Crea una nueva instancia del procesador de combinación de correspondencia. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Ejecutar la acción del procesador. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el archivo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el archivo de salida para el procesador. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_12)(*string, string, DataRow*) | Realiza la combinación de correspondencia desde un DataRow al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_13)(*string, string, DataTable*) | Realiza la fusión de correspondencia desde un DataTable al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_14)(*string, string, string[], object[]*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_4)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_6)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataRow al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_7)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataRow al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_9)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataRow al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_10)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataRow al documento. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_2)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_5)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_8)(*string, string, [SaveFormat](../../aspose.words/saveformat/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [Execute](../../aspose.words.lowcode/mailmerger/execute/#execute_11)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataRow, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_4)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un DataRow al documento y procesa el resultado en imágenes. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_2)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro y convierte el resultado en imágenes. |
| static [ExecuteToImages](../../aspose.words.lowcode/mailmerger/executetoimages/#executetoimages_5)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), string[], object[], [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro y convierte el resultado en imágenes. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_8)(*string, string, DataSet*) | Realiza una fusión de correspondencia desde un conjunto de datos a un documento con regiones de fusión de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_9)(*string, string, DataTable*) | Realiza la combinación de correspondencia desde un DataTable al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un conjunto de datos al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un conjunto de datos al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_3)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza una operación de combinación de correspondencia para un solo registro. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_4)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un conjunto de datos al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataTable al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un conjunto de datos al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegions](../../aspose.words.lowcode/mailmerger/executewithregions/#executewithregions_7)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde un DataTable al documento con regiones de combinación de correspondencia. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un conjunto de datos en el documento con regiones de fusión de correspondencia y procesa el resultado en imágenes. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_1)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde una DataTable al documento con regiones de combinación de correspondencia y procesa el resultado en imágenes. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_2)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataSet, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la fusión de correspondencia desde un conjunto de datos en el documento con regiones de fusión de correspondencia y procesa el resultado en imágenes. |
| static [ExecuteWithRegionsToImages](../../aspose.words.lowcode/mailmerger/executewithregionstoimages/#executewithregionstoimages_3)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), DataTable, [MailMergeOptions](../mailmergeoptions/)*) | Realiza la combinación de correspondencia desde una DataTable al documento con regiones de combinación de correspondencia y procesa el resultado en imágenes. |

### Ver también

* class [Processor](../processor/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
