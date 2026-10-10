---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify method"
linktitle: "Notify"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::IDocumentSavingCallback::Notify. Viene chiamato per notificare l'avanzamento del salvataggio del documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Questo è chiamato per notificare l'avanzamento del salvataggio del documento.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| argomenti | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Un argomento dell'evento. |
## Note


Gli usi principali di questa interfaccia sono consentire al codice dell'applicazione di ottenere lo stato di avanzamento e di interrompere il processo di salvataggio.

Un'eccezione dovrebbe essere lanciata dal callback di avanzamento per l'interruzione e dovrebbe essere catturata nel codice del consumatore.

## Vedi anche

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
