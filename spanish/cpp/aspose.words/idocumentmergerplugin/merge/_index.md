---
title: "Aspose::Words::IDocumentMergerPlugin::Merge método"
linktitle: "Combinar"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::IDocumentMergerPlugin::Merge método. Combina los documentos PDF de entrada proporcionados en un único documento PDF de salida utilizando los flujos de entrada y salida especificados en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/idocumentmergerplugin/merge/
---
## IDocumentMergerPlugin::Merge method


Combina los documentos PDF de entrada proporcionados en un único documento PDF de salida utilizando los flujos de entrada y salida especificados.

```cpp
virtual void Aspose::Words::IDocumentMergerPlugin::Merge(System::SharedPtr<System::IO::Stream> outputStream, System::ArrayPtr<System::SharedPtr<System::IO::Stream>> inputStreams, System::ArrayPtr<System::SharedPtr<Aspose::Words::Loading::LoadOptions>> loadOptions)=0
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| outputStream | System::SharedPtr\<System::IO::Stream\> | El flujo de salida. |
| inputStreams | System::ArrayPtr\<System::SharedPtr\<System::IO::Stream\>\> | Los flujos de entrada. |
| loadOptions | System::ArrayPtr\<System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\> | Opciones de carga para los archivos de entrada. |

## Ver también

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Interface [IDocumentMergerPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
