---
title: Merger.MergeToImages
linktitle: MergeToImages
articleTitle: MergeToImages
second_title: Aspose.Words para .NET
description: Combine varios documentos sin esfuerzo con el método MergeToImages, creando una única salida de imagen mientras personaliza los nombres de los archivos y las opciones de guardado.
type: docs
weight: 30
url: /es/net/aspose.words.lowcode/merger/mergetoimages/
---
## MergeToImages(*string[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages_1}

Fusiona los documentos de entrada dados en un único documento de salida utilizando los nombres de archivo de entrada y salida especificados y las opciones de guardado. Representa la salida en imágenes.

```csharp
public static Stream[] MergeToImages(string[] inputFiles, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputFiles | String[] | Los nombres de los archivos de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)

---

## MergeToImages(*Stream[], [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), [MergeFormatMode](../../mergeformatmode/)*) {#mergetoimages}

Fusiona los flujos de documentos de entrada dados en un único documento de salida utilizando las opciones de guardado de imágenes especificadas. Representa la salida en imágenes.

```csharp
public static Stream[] MergeToImages(Stream[] inputStreams, ImageSaveOptions saveOptions, 
    MergeFormatMode mergeFormatMode)
```

| Parámetro | Escribe | Descripción |
| --- | --- | --- |
| inputStreams | Stream[] | Los flujos de archivos de entrada. |
| saveOptions | ImageSaveOptions | Las opciones de guardado. |
| mergeFormatMode | MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

### Ver también

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* enum [MergeFormatMode](../../mergeformatmode/)
* class [Merger](../)
* espacio de nombres [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* asamblea [Aspose.Words](../../../)
