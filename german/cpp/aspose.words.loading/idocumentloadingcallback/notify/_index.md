---
title: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify Methode"
linktitle: "Notify"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify method. Dies wird aufgerufen, um über den Fortschritt des Dokumentladens in C++ zu benachrichtigen."
type: docs
weight: 4000
url: /de/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Dies wird aufgerufen, um über den Fortschritt des Dokumentladens zu benachrichtigen.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Ein Argument des Ereignisses. |
## Hinweise


Der Hauptzweck dieser Schnittstelle besteht darin, Anwendungscode zu ermöglichen, den Fortschrittsstatus zu erhalten und den Ladevorgang abzubrechen.

Eine Ausnahme sollte vom Fortschritts-Callback für den Abbruch ausgelöst werden und im Verbraucher-Code abgefangen werden.

## Siehe auch

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
