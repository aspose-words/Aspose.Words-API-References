---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify Methode"
linktitle: "Notify"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Saving::IDocumentSavingCallback::Notify Methode. Diese wird aufgerufen, um über den Fortschritt des Dokumentspeicherns in C++ zu benachrichtigen."
type: docs
weight: 4000
url: /de/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Dies wird aufgerufen, um über den Fortschritt des Dokumentenspeicherns zu benachrichtigen.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| args | System::SharedPtr\\<Aspose::Words::Saving::DocumentSavingArgs\\> | Ein Argument des Ereignisses. |
## Hinweise


Der Hauptzweck dieser Schnittstelle besteht darin, Anwendungscode zu ermöglichen, den Fortschrittsstatus abzurufen und den Speicherungsprozess abzubrechen.

Eine Ausnahme sollte vom Fortschritts-Callback für den Abbruch ausgelöst werden und im Verbraucher-Code abgefangen werden.

## Siehe auch

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
