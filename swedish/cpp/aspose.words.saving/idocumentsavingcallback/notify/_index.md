---
title: "Aspose::Words::Saving::IDocumentSavingCallback::Notify method"
linktitle: "Notify"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::IDocumentSavingCallback::Notify method. Detta anropas för att meddela om dokumentets sparningsförlopp i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Detta anropas för att meddela dokumentets sparningsförlopp.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Ett argument till händelsen. |
## Anmärkningar


Det primära användningsområdet för detta gränssnitt är att låta applikationskod hämta förloppsstatus och avbryta sparningsprocessen.

Ett undantag bör kastas från framstegskallbacken för avbrytning och det bör fångas i konsumentkoden.

## Se även

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
