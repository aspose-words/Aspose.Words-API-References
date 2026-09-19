---
title: "Metodo Read di Aspose::Words::IDocumentReaderPlugin"
linktitle: "Read"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Read di Aspose::Words::IDocumentReaderPlugin. Legge i dati dallo stream specificato nell'istanza Document in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/idocumentreaderplugin/read/
---
## IDocumentReaderPlugin::Read method


Legge i dati dallo stream specificato nell'istanza [Document](../../document/).

```cpp
virtual void Aspose::Words::IDocumentReaderPlugin::Read(System::SharedPtr<System::IO::Stream> src, System::SharedPtr<Aspose::Words::Loading::LoadOptions> loadOptions, System::SharedPtr<Aspose::Words::Document> document)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| src | System::SharedPtr\<System::IO::Stream\> | Lo stream di origine da cui leggere il documento. |
| loadOptions | System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> | Opzioni di caricamento aggiuntive per caricare il documento. |
| document | System::SharedPtr\<Aspose::Words::Document\> | L'istanza della classe [Document](../../document/) in cui leggere i dati. Se l'istanza contiene del contenuto, verrà sovrascritto dai dati dello stream di origine. |

## Vedi anche

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [Document](../../document/)
* Interface [IDocumentReaderPlugin](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
