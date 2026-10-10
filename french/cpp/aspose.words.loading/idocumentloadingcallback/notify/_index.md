---
title: "Méthode Aspose::Words::Loading::IDocumentLoadingCallback::Notify"
linktitle: "Notify"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Loading::IDocumentLoadingCallback::Notify. Elle est appelée pour notifier de la progression du chargement du document en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.loading/idocumentloadingcallback/notify/
---
## IDocumentLoadingCallback::Notify method


Ceci est appelé pour notifier de la progression du chargement du document.

```cpp
virtual void Aspose::Words::Loading::IDocumentLoadingCallback::Notify(System::SharedPtr<Aspose::Words::Loading::DocumentLoadingArgs> args)=0
```


| Paramètre | Type | Description |
| --- | --- | --- |
| args | System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\> | Un argument de l'événement. |
## Remarques


L'utilisation principale de cette interface est de permettre au code de l'application d'obtenir le statut de progression et d'interrompre le processus de chargement.

Une exception doit être levée depuis le rappel de progression pour l'annulation et elle doit être capturée dans le code du consommateur.

## Voir aussi

* Class [DocumentLoadingArgs](../../documentloadingargs/)
* Interface [IDocumentLoadingCallback](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
