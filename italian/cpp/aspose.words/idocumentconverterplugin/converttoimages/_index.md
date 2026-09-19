---
title: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method"
linktitle: "ConvertToImages"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IDocumentConverterPlugin::ConvertToImages method. Converte le pagine del documento dallo stream di input in un array di immagini in C++."
type: docs
weight: 2500
url: /it/cpp/aspose.words/idocumentconverterplugin/converttoimages/
---
## IDocumentConverterPlugin::ConvertToImages method


Converte le pagine del documento dal flusso di input a un array di immagini.

```cpp
virtual System::ArrayPtr<System::SharedPtr<System::IO::Stream>> Aspose::Words::IDocumentConverterPlugin::ConvertToImages(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Il flusso di input. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Le opzioni di caricamento del documento. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Le opzioni di salvataggio. |

### ReturnValue

Array di stream di immagini delle pagine.

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
