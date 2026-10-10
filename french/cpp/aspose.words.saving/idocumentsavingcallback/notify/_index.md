---
title: "Méthode Notify de Aspose::Words::Saving::IDocumentSavingCallback"
linktitle: "Notify"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Notify de Aspose::Words::Saving::IDocumentSavingCallback. Elle est appelée pour notifier de la progression de l'enregistrement du document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/idocumentsavingcallback/notify/
---
## IDocumentSavingCallback::Notify method


Ceci est appelé pour notifier de la progression de l'enregistrement du document.

```cpp
virtual void Aspose::Words::Saving::IDocumentSavingCallback::Notify(System::SharedPtr<Aspose::Words::Saving::DocumentSavingArgs> args)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\> | Un argument de l'événement. |
## Remarques


Les utilisations principales de cette interface sont de permettre au code applicatif d'obtenir le statut de progression et d'interrompre le processus d'enregistrement.

Une exception doit être levée depuis le rappel de progression pour l'annulation et elle doit être capturée dans le code du consommateur.

## Voir aussi

* Class [DocumentSavingArgs](../../documentsavingargs/)
* Interface [IDocumentSavingCallback](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
