---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages método"
linktitle: "ConvertToImages"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages método. Convierte páginas del documento desde el flujo de entrada a una matriz de imágenes en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Convierte páginas del documento desde el flujo de entrada a una matriz de imágenes.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | El flujo de entrada. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Las opciones de carga del documento. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Las opciones de guardado. |

### ReturnValue

Matriz de flujos de imágenes de página.

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
