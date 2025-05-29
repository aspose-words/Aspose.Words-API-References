---
title: Merger Class
linktitle: Merger
articleTitle: Merger
second_title: Aspose.Words para .NET
description: Combine fácilmente diversos tipos de documentos en uno solo con la clase Aspose.Words.LowCode.Merger. ¡Optimice su flujo de trabajo y mejore su productividad hoy mismo!
type: docs
weight: 4300
url: /es/net/aspose.words.lowcode/merger/
---
## Merger class

Representa un grupo de métodos destinados a fusionar una variedad de diferentes tipos de documentos en un único documento de salida.

```csharp
public class Merger : Processor
```

## Métodos

| Nombre | Descripción |
| --- | --- |
| static [Create](../../aspose.words.lowcode/merger/create/#create)() | Crea una nueva instancia del procesador de combinación de correspondencia. |
| static [Create](../../aspose.words.lowcode/merger/create/#create_1)(*[MergerContext](../mergercontext/)*) | Crea una nueva instancia del procesador de combinación de correspondencia. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Ejecutar la acción del procesador. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Especifica el documento de entrada para su procesamiento. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica la lista de flujos de documentos de salida. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el flujo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Especifica el archivo de salida para el procesador. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Especifica el archivo de salida para el procesador. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge)(*Document[], [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un solo documento y devuelve[`Document`](../../aspose.words/document/) instancia del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_2)(*Stream[], [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un solo documento y devuelve[`Document`](../../aspose.words/document/) instancia del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_8)(*string, string[]*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados utilizandoKeepSourceFormatting . |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_4)(*string[], [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un solo documento y devuelve[`Document`](../../aspose.words/document/) instancia del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_6)(*Stream, Stream[], [SaveFormat](../../aspose.words/saveformat/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando flujos de entrada y salida especificados y el formato del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_1)(*Stream[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un solo documento y devuelve[`Document`](../../aspose.words/document/) instancia del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_3)(*string[], LoadOptions[], [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un solo documento y devuelve[`Document`](../../aspose.words/document/) instancia del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_7)(*Stream, Stream[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando flujos de entrada y salida especificados y opciones de guardado. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_10)(*string, string[], [SaveFormat](../../aspose.words/saveformat/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados y el formato del documento final. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_11)(*string, string[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_5)(*Stream, Stream[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando flujos de entrada y salida especificados y opciones de guardado. |
| static [Merge](../../aspose.words.lowcode/merger/merge/#merge_9)(*string, string[], LoadOptions[], [SaveOptions](../../aspose.words.saving/saveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages)(*Stream[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los flujos de documentos de entrada dados en un único documento de salida utilizando las opciones de guardado de imágenes especificadas. Representa la salida en imágenes. |
| static [MergeToImages](../../aspose.words.lowcode/merger/mergetoimages/#mergetoimages_1)(*string[], [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../mergeformatmode/)*) | Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado. Representa la salida en imágenes. |

## Observaciones

Los archivos o secuencias de entrada y salida especificados, junto con las opciones de combinación y guardado deseadas, se utilizan para combinar los documentos de entrada dados en un solo documento de salida.

La funcionalidad de fusión admite más de 35 formatos de archivos diferentes.

## Ejemplos

Muestra cómo fusionar documentos en un único documento de salida.

```csharp
//Hay varias formas de fusionar documentos:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ver también

* class [Processor](../processor/)
* espacio de nombres [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../)
