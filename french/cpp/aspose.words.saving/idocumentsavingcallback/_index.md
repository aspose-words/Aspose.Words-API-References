---
title: "Aspose::Words::Saving::IDocumentSavingCallback interface"
linktitle: "IDocumentSavingCallback"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::IDocumentSavingCallback interface. Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors de l'enregistrement d'un document en C++."
type: docs
weight: 41000
url: /fr/cpp/aspose.words.saving/idocumentsavingcallback/
---
## IDocumentSavingCallback interface


Implémentez cette interface si vous souhaitez disposer de votre propre méthode personnalisée appelée lors de l'enregistrement d'un document.

```cpp
class IDocumentSavingCallback : public virtual System::Object
```

## Méthodes

| Méthode | Description |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Saving::DocumentSavingArgs\>) | Ceci est appelé pour notifier de la progression de l'enregistrement du document. |
| static [Type](./type/)() |  |
## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
