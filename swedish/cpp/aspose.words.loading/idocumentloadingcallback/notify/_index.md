---
title: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify‑metod"
linktitle: "Notify"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Loading::IDocumentLoadingCallback::Notify‑metod. Denna kallas för att meddela om dokumentladdningsprogress i C++."
type: docs
weight: 4000
url: /sv/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Detta anropas för att meddela dokumentladdningsförloppet.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Ett argument till händelsen. |
## Anmärkningar


Det primära användningsområdet för detta gränssnitt är att låta applikationskod hämta status för framsteg och avbryta laddningsprocessen.

Ett undantag bör kastas från framstegskallbacken för avbrytning och det bör fångas i konsumentkoden.

## Se även

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
