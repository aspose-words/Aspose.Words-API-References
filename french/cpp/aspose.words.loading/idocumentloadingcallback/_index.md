---
title: "Aspose::Words::Loading::IDocumentLoadingCallback interface"
linktitle: "IDocumentLoadingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Loading::IDocumentLoadingCallback interface. Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors du chargement d'un document en C++."
type: docs
weight: 10000
url: /fr/cpp/aspose.words.loading/idocumentloadingcallback/
---
## IDocumentLoadingCallback interface


Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors du chargement d'un document.

```cpp
class IDocumentLoadingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Loading::DocumentLoadingArgs\>) | Ceci est appelé pour notifier de la progression du chargement du document. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Loading](../)
* Library [Aspose.Words for C++](../../)
