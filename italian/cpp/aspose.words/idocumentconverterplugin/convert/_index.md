---
title: "Metodo Aspose::Words::IDocumentConverterPlugin::Convert"
linktitle: "Converti"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::IDocumentConverterPlugin::Convert method. Converte il documento utilizzando i flussi di input e output specificati e le opzioni di salvataggio in C++."
type: docs
weight: 2000
url: /it/cpp/aspose.words/idocumentconverterplugin/convert/
---
## IDocumentConverterPlugin::Convert method


Converte il documento utilizzando i flussi di input/output specificati e le opzioni di salvataggio.

```cpp
virtual void Aspose::Words::IDocumentConverterPlugin::Convert(System::SharedPtr<System::IO::Stream> inputStream, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<System::IO::Stream> outputStream, System::SharedPtr<Aspose::Words::Saving::SaveOptions> saveOptions)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| inputStream | System::SharedPtr\<System::IO::Stream\> | Il flusso di input. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Le opzioni di caricamento del documento. |
| outputStream | System::SharedPtr\<System::IO::Stream\> | Lo stream di output. |
| saveOptions | System::SharedPtr\<Aspose::Words::Saving::SaveOptions\> | Le opzioni di salvataggio. |

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* Interface [IDocumentConverterPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
