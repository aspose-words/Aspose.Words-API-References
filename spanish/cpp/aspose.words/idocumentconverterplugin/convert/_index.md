---
title: "Método Aspose::Words::IDocumentConverterPlugin::Convert"
linktitle: "Convertir"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IDocumentConverterPlugin::Convert method. Convierte el documento usando los flujos de entrada y salida especificados y las opciones de guardado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


Convierte el documento usando los flujos de entrada y salida especificados y las opciones de guardado.

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | El flujo de entrada. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Las opciones de carga del documento. |
| outputStream | System::SharedPtr\<System::IO::Stream\> | El flujo de salida. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Las opciones de guardado. |

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
