---
title: "Aspose::Words::LowCode::Merger::MergeToImages método"
linktitle: "MergeToImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::LowCode::Merger::MergeToImages método. Fusiona los flujos de documentos de entrada proporcionados en un único documento de salida utilizando las opciones de guardado de imagen especificadas. Renderiza la salida a imágenes en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.lowcode/merger/mergetoimages/
---
## Merger::MergeToImages(const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Fusiona los flujos de documentos de entrada proporcionados en un único documento de salida usando las opciones de guardado de imagen especificadas. Renderiza la salida a imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::SharedPtr<System::IO::Stream>> &inputStreams, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStreams | const System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\>\& | Los flujos de archivos de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
## Merger::MergeToImages(const System::ArrayPtr\<System::String\>\&, const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\&, Aspose::Words::LowCode::MergeFormatMode) method


Fusiona los documentos de entrada proporcionados en un único documento de salida usando los nombres de archivo de entrada y salida especificados y las opciones de guardado. Renderiza la salida a imágenes.

```cpp
static System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::LowCode::Merger::MergeToImages(const System::ArrayPtr<System::String> &inputFiles, const System::SharedPtr<Aspose::Words::Saving::ImageSaveOptions> &saveOptions, Aspose::Words::LowCode::MergeFormatMode mergeFormatMode)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputFiles | const System::ArrayPtr\<System::String\>\& | Los nombres de archivo de entrada. |
| saveOptions | const System::SharedPtr\<Aspose::Words::Saving::ImageSaveOptions\>\& | Las opciones de guardado. |
| mergeFormatMode | Aspose::Words::LowCode::MergeFormatMode | Especifica cómo fusionar el formato que entra en conflicto. |

## Ver también

* Class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* Enum [MergeFormatMode](../../mergeformatmode/)
* Class [Merger](../)
* Namespace [Aspose::Words::LowCode](../../)
* Library [Aspose.Words for C++](../../../)
