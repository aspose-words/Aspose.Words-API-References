---
title: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify metodo"
linktitle: "Notify"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify metodo. Questo è chiamato per notificare lo stato di avanzamento del caricamento del documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Viene chiamato per notificare l'avanzamento del caricamento del documento.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| argomenti | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Un argomento dell'evento. |
## Note


Gli usi principali di questa interfaccia sono consentire al codice dell'applicazione di ottenere lo stato di avanzamento e di interrompere il processo di caricamento.

Un'eccezione dovrebbe essere lanciata dal callback di avanzamento per l'interruzione e dovrebbe essere catturata nel codice del consumatore.

## Vedi anche

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
